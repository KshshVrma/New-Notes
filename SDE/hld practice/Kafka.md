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