internally sql joins are mainly executed in these three ways->

nested loop: like an n^2 loop eg

for r1 in table1:
	for r2 in table2:
			if r1.id=r2.id:
				xxxx
Sort: both the tables are sorted and then mapped 
		here too preparation is required. 

Hashing:
	preparation is required to hash the id of the tables, post that it is a very efficient approach to join a table.
[[ACID props]]