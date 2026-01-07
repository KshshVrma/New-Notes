![[Pasted image 20251011155626.png]]


it is a pull based message queue, whereas generally a message queue si either supposed to be either point2point or pub sub model, in kafka consumers constantly poll for any new messages in the queue.

here the producers send the message to a cluster of brokers,
within a cluster there are multiple brokers which are managed by the zookeeper.

withing a broker we have a topic and under a topic we have partitions, partitions are the places where the actual data is stored and so some things to keep in mind,
the consumer group contains different consumers, and each consumer within the same consumer group must consume messages from a different partition and they cannot consumer message from multiple partitions.
if one consumer goes down and there is a free consumer within a consumer group then simply we assign the partioin to be consumed by a different consumer.

within a cluster there are multiple brokers which might maintain a copy for a partition eg in broker 1 we may store topic a partition 0 and in broker 2 we may store topic a partition 2, 

generally we maintain a copy as well for each of the partitions in different brokers in case the partition fails.

we generally store the messsage in this format:
topic
key
value
partition

additionally the zookeeper maintains the status of the data that has been consumed by the consumer in case it is to be assigned to a new consumer, eg if the offset is 3 then we know that till index 3 all the data has been actually read and in case we need to assigne that partition to another consumer in that case simply we can start from offset +1 as till offset we already have it consumed.

for each partition we can assigne the number of times any consumer can retry to consume the message eg 3 times.


# 🏗️ **Kafka — HLD Notes (Interview-Focused)**

## 1️⃣ Problem Kafka Solves (HLD framing)

### Traditional problem

Backend systems need to handle:

- Massive event/log data
    
- Multiple consumers (real-time + batch)
    
- High throughput
    
- Fault tolerance
    
- Reprocessing capability
    

### Why queues fail

Traditional message queues (JMS, RabbitMQ):

- Push-based → consumer overload
    
- Broker tracks message state → poor scalability
    
- Designed for short-lived messages
    
- Hard to replay data
    

👉 **Kafka reframes the problem as distributed log storage**, not just messaging.

---

## 2️⃣ Core Abstraction (Most Important)

### Kafka = **Distributed Append-Only Log**

- Data is **never updated or deleted immediately**
    
- Messages are appended sequentially
    
- Consumers read at their own pace using offsets
    

This single decision drives:

- Scalability
    
- Performance
    
- Replayability
    
- Simplicity
    

---

## 3️⃣ High-Level Architecture

`Producer → Topic → Partition → Broker                       ↑                  Consumer Group`

### Core components

- **Producer**: publishes events
    
- **Topic**: logical stream
    
- **Partition**: ordered log
    
- **Broker**: stores partitions
    
- **Consumer**: reads events
    
- **Consumer Group**: parallel consumption
    

---

## 4️⃣ Topics & Partitions (Scalability Model)

### Topic

- Logical grouping of events
    
- Example: `order-events`
    

### Partition

- Unit of:
    
    - Storage
        
    - Ordering
        
    - Parallelism
        

**Rules**

- Order guaranteed **within a partition**
    
- No order guarantee across partitions
    
- One partition → one consumer per group
    

👉 **Parallelism = number of partitions**

---

## 5️⃣ Producer Design (Write Path)

### Key ideas

- Writes are **append-only**
    
- Messages batched for efficiency
    
- Partition selection via:
    
    - Key hash (ordering use cases)
        
    - Round-robin (load distribution)
        

### Why this scales

- Sequential disk writes
    
- No random I/O
    
- Minimal metadata per message
    

---

## 6️⃣ Consumer Design (Read Path)

### Pull-based model

- Consumer explicitly fetches data
    
- Controls its own speed
    
- Can pause, resume, rewind
    

### Offset-based consumption

- Offset = logical position in log
    
- Consumer stores offset
    
- Broker is stateless
    

👉 Enables:

- Reprocessing
    
- Backfill
    
- Offline analytics
    

---

## 7️⃣ Consumer Groups (Load Balancing)

### How it works

- Each partition assigned to one consumer per group
    
- Multiple consumers → parallel reads
    
- Automatic rebalancing on join/leave/failure
    

### Trade-off

- Rebalancing causes temporary pauses
    
- Accepted for scalability
    

---

## 8️⃣ Storage Design (Why Kafka Is Fast)

### Log Segments

- Each partition → multiple segment files
    
- Fixed size (e.g., 1GB)
    
- Old segments deleted based on retention
    

### OS Page Cache

- Kafka avoids JVM caching
    
- Relies on OS cache
    
- Benefits:
    
    - Less GC
        
    - Faster restarts
        
    - Predictable performance
        

### Zero-Copy Transfer

- Uses `sendfile()`
    
- Data moves disk → network directly
    
- Fewer memory copies
    

---

## 9️⃣ Delivery Guarantees (Design Trade-offs)

### Guarantees

- **At-least-once delivery**
    
- **In-order per partition**
    
- No exactly-once in base design
    

### Why not exactly-once?

- Requires 2PC
    
- Adds latency
    
- Reduces throughput
    

👉 Kafka prefers:

> **Simplicity + performance over strong semantics**

Applications handle:

- Deduplication
    
- Idempotency
    

---

## 🔟 Failure Handling

### Broker failure

- Unreplicated data may be lost (in original paper)
    
- Consumers can resume from last committed offset
    

### Data corruption

- CRC per message
    
- Corrupt messages skipped
    

Kafka assumes:

- Failures happen
    
- Systems should recover quickly
    

---

## 1️⃣1️⃣ Coordination (ZooKeeper – paper version)

Used for:

- Broker discovery
    
- Consumer group membership
    
- Partition ownership
    
- Offset storage
    

Centralized coordination simplifies:

- Failure detection
    
- Rebalancing
    

(Modern Kafka replaces this with internal metadata quorum, but **concept remains same**.)

---

## 1️⃣2️⃣ Performance Characteristics (HLD Gold)

### Why Kafka outperforms queues

- Sequential disk I/O
    
- Batch writes & reads
    
- No per-message ACK
    
- Stateless brokers
    
- Pull-based consumers
    

### Result

- Hundreds of thousands of messages/sec
    
- Low latency even with large backlogs
    

---

## 1️⃣3️⃣ Typical Use Cases (Interview Examples)

- Event sourcing
    
- Activity tracking
    
- Log aggregation
    
- Stream processing
    
- CDC (Change Data Capture)
    
- Real-time analytics
    
- Microservices communication
    

---

## 1️⃣4️⃣ Design Trade-offs (Always Mention)

|Decision|Benefit|Cost|
|---|---|---|
|Log abstraction|Replay, scale|More app responsibility|
|Pull model|Consumer control|Slight latency|
|Partition ordering|High throughput|No global ordering|
|At-least-once|Simple, fast|Dedup needed|

---

## 1️⃣5️⃣ How to Explain Kafka in Interviews (Template)

> Kafka is a distributed messaging system built around an append-only log abstraction.  
> Data is written sequentially to partitioned logs, and consumers pull data using offsets, allowing replay and parallel consumption.  
> Kafka prioritizes throughput and scalability by using sequential disk I/O, batching, stateless brokers, and OS-level optimizations, while intentionally trading off strong delivery guarantees.

---

## 🧠 Common Interview Follow-ups (Be Ready)

1. Why is Kafka pull-based?
    
2. Why is partition-level ordering sufficient?
    
3. How does Kafka handle consumer failures?
    
4. When would you NOT use Kafka?
    
5. Kafka vs RabbitMQ vs Pulsar?
    
6. How does replay help in debugging?