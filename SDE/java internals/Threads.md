in java if you want to make use of threads then you have to mainly use one of these 3 :
Thread class which internally implements runnable interface here we need to define a run method, inorder to invoke it we need to create an object and call the .start() method which will start the .run() method in the class that we overwrote from the interface runnable

runnable is a interface that can be implemented , which inturn needs to be passed manually to a thread object inorder for the start to be called.
this is like a blue print for the thread to execute and depends on a thread object for actualy invocation.. btw both theads and runnable objects can be initialized using ananumous class and runnable can be implemented using lambda notation as well..

executor service is something which manages different threads and we have to pass the runnable objects to it, it internally manages the threads which are assigned to it in the maxthreadpool call, however it uses internal algorithms including a queue to efficiently manage the task to be actually run.

if the task is given and the current working threads are less than the core thread size ie the number of assigned threads in that case we directly assign the task. if they are busy we append to a queue which stores the task, if the queue is full in that case we simply create new threads and assign the task to the new threads till the number of created thereads are less than the max possible threads assigned to it.  when all the executions are done it calls a shutdown and stops all the threads.