

these are 4 database properties , all being followed in an ideal case however tradeoffs do exist, and based on the situation of the task more weightage should be given to the property.

A: atomicity:

either the transction happens completely or it reverts back
this can be achieved through transaction blocks in the db

C: consistency
suppose the database has been sharded, and we update one of the shards, 
... now if before the shards are synced we do a read operation on another shard in that case the consistency will be effected, and we would not be able to see our latest changes.
one soultion is to follow something like a master/slave combination..

D: durability:
change when commited should always reflect:
suppose there is a db, which colectes all the update queries, and inserts them togerther in a batch.. to the long term storage ie the disk. so now if in between power goes out and supposed one of the inserts was commited but not written to the disk then durabililty fails.

.. redis solved this though providing options for taking snapshots of the db, frequently.

I: isolation:

suppose if there is a transaction going on 
alice pays bob 10 rs.
now if the amount has been debited from alice but not yet reached bob. and we query the sum of balance of alice and bob's account, in that case we would find this 10 rs missing...
solution could be to have some sort of locking mechanism..
