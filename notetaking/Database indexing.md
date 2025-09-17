database indexing is an important property , it can massively improve the performance of the database, 

in normal operations if the database is not indexed then the read operation is done for all the blocks of the dataase.

** point to note is that suppose if we query a row which is of x bytes, not only those x bytes are read but to extract any byte the system has to read an entire block of memory , .. which makes this very inefficient process, and so , if there are 100 rows and suppose they are not index , the data might be spread across 35 blocks of memory , now if we create an index on the data that we need and query the database based on the index, in that scenario :
suppose the index takes 2 blocks of memory, and the result of the query that you want to read is in 3 different blocks( if the mapping of block and row is done in the index) the total time taken to query the database is now only 5 seconds, so..overall improvement is huge as the performance is improved 7 times compared to the reaad operation without creating any indexes .

[[SQL Joins]]