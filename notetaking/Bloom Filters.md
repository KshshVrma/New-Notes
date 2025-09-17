[[Redis]]

these are a type of data structure which is used to implement sets, at scale.
as lookups at a large scale not only require log n time lookup but also consume a large amount of data as a set which represents and entire entity, think of youtube videos can itself take gigantic amount of memory.

The datastructure sets usually are built on top of self balancing binary trees, there fore even if they are extremely efficient int ther terms of time complexity but they do require and have adiitional overhead of storing poitners, think right and left pointers fo the binary tree.
this leads the metadata to be bloated and to require even more data than the object itself which is not very efficient and specially in the scenarios wehr  memory is more critical ,eg think mars rovers/ iot devices / embedded systmes. this is a deal breaker.

The main function that is supported by bloom filters is o tthell whether an element is already presne t in the main database, and in order to achieve this we decide on a tradeoff that we no longer would be storing the data as it is. but we would imporovise a bit on it so that we make lookup times extremely fast.

So one of the implementations of bloom fileters can be like this.:
for every object we create a hash value and we mark the hash value obtained to be visited , now we have a list of all the hash values visisted which means that whenven we have a object which ahs not being stored in the database , then it is very easy to identify that , by just calculating the hash value fo the new data and checking if the value is present in the simple storage array / markup array that we are using .

this approach quickly identifies the false negatives are not possible with blommm filter, however the problem comes when storing somethign which already has a hash value similary to any previously hashed element. so in case of has collision we need to figure out a solution , do we now query the main database in order to check? or we imporvidse and use techiniques that we normally use for solgving hash collisions, this can be decidied to be done on the use-case basis.

one of the main advantages/ suecases of bloom filters is in determining if a username has been taken or not, this is very critical for big data sourced companies like google or amazon where the data of the number of users is in billinos, so if the username is not present in that scenario with useing bloom filters as part of  the solution we can quickly determine if the user has been taken or not..
 some considerations: 
 in case of hash collisions we can make use of secondary solutions like redis cache.
 as the data need to be in sync with the database we constantly need to check updates form the min database, but this can be done concurrrently and this process can be done in the background without affecting the data structures functionality.