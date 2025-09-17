whenever a hashmap hits certain load of data present ie percentage of storage which is filled .
normally it doubles in size:


number/thing-> hash funciton-> x -> mod size of map-> index

now one of the mean reasons we double the size of map and retain it to a size of 1, 2,4, 8,16,... because in binary the number is represnted as 100...

the point being for example if we have the size as 4 then the mod 4 maps to :
0, 1, 2, 3, 0, 1,2, 3,...

and the thing to point out is that mod operations are not very efficient , as compared to other bitwise operators.

so the clever solution is that for numbers which are of power 2,
this mod pattern is equivalent to (2^n-1)& number;

eg in the above example 0&3, 1&3, 2&3, 3&3... will provide the same pattern and is also much faster to execute.