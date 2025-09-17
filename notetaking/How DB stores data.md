varchar, has a limit and the entry will fail if exceeded, but the columns can act as a foreign key.

text, has no limit, but cannot be used as foreign keys,

string, this data type appends black spaces to fill the remaining size, not recommend to be used, neither space efficient, nor unique in any way.

int : data can be stored as varint ie as a bit array, for eg if the first section of the bit array is of 8 bits, then the last ie the 8th bit can be used as a continuation bit so if the integer takes more than 7 bits then the continuation bit turns to be 1, using this for small numbers we only require small spaces, but large numbers do require more space, also we need more computation power to encode and decode integers.



[[SQL Joins]]