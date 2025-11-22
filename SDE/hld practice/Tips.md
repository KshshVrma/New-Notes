
Rate limiting:
leaking bucket: 
token based limiting: has n tokens with refresh rate of r per minute, each new request requires one new token.
and each token is associated with the new request. 
these are assigned per user , eg per ip. these can be cached using redis.

database:
Dynamo db and Cassandra adopt eventual consistency across distributed datastores, which is recommended consistency model for our key value store.

versioning can be used to solve inconsistency across distributed data sources.

Gossip protocol: To check if a node is down in a distributed system we can make use of heartbeats.
each node propagates to a decentralized system or other set of random nodes a timestamp during which it is active, these random node can propagate to other node, one node can be considered failed if ithas not sent any update within a time period.

Key value datastore: distributed:

![[Pasted image 20251122214929.png]]