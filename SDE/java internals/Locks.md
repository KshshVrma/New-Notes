locks behave in a similar manner to the synchronized keyword however they are more flexible , as they can be controlled in a better way :
whenever we use the synchronize keyword we are basically acquiring an intrinsic lock which is freed only when the block ends,

meanwhile for example we can also use locks like:

reentrant lock
for using any implicit lock we normally implement the lock interface so kind of like 

Lock lock =new reentrant lock;

this can be extremely useful as it contains some useful methods like:

lock.lock();: acquires a lock similar to synchronized block
lock.unlock(); unlocks the acquired lock
lock.trylock(); if block is not in use it will lock it, else will return saying that resourse is already in use.
lock.trylock(1000, time.millisecond); will wait for 1000ms if the resource is already locked, however if still the resource remains locked then it will return without executing.

the benefit of reentrant lock is that the thread which has aquired the lock can call the lock.lock method again under any subblock or a submethod which means that the code is deadlock proof and therefore can be used

internally it follows a  counter mechanism;
so eg

outer block{
lock.lock
innerblock();
lock.unlock();
}

inner block{
lock.lock
sout abc
lock.unlock
}

//this sequence of operation is possible. because we can again call lock.lock when we are using reentrant lock
