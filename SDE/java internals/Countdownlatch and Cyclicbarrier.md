
when we need to control the behavour of multiple threads executing some of the useful classes that we can use is countdownlatch and cyclicbarrier

countdownlatch:

suppose you have multiple threads executing multiple task , however upon completion of them you want to execute something ie block the main thread till the execution of all the threads is complete so you can make use of countdownlatch
countdownlatch ctl=new countdownlatch(3);

now add this as a field in the classes that you are passing to the threads either manually or using executeservice theadpool, and then simply make use of the countdown() method when you want to do the countdown ie mark the thread as complete.

at the end we call a ctl.await() the main thread will wait here till the count becomes 0;

it's useful for a limited usecase it's like you are the race manager and want the race contestants to finish before announding the winner.
but this is not reusable.

cyclicbarrier is a class that can be used in a similar manner but instead of calling await at the end we simply call the .await method in one of the execution methods, the great part is that untill all the threads complete and reacch their respective  await calls the execution won't move forward. once the final threads too reach the .await all the threads resume.