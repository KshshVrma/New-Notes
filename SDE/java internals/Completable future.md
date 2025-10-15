In java if we want to run any portion of the code asyncronously then in that case we can make use  of the completablefuture, it has useful set of methods which solve a lot of problem in the wsense that they allow the code to run in a seperate thread, allows chaining of events that too asyncronously without blocking the main thread from executing 

some of the useful methods include
supply returns a value upon completion of the method
run runs without returning any value

it can be chained with .thenapply and .thenaccept where we can chain a list of task which are going to run asynchronously 

finally you can run the .get that is a blocking call that allows the main thread to run only post the execution of the future has stopped.

some more useful methods include:
allof
anyof, etc.

these 3 are especially important:

.thenapply : this simply does a mapping of the output that the supply returns.
it's like adding salt to food after food is prepared.


.thencompose: this allows execution of multiple completable future blocks one after the other thus ensuring that. any asynchronous task that depends on one of the asynchronous task can get executed.
it's like ordering desert after eating the maindish is over

.thencombine: this allows multiple  async tasks to finish and then we performing some operation on each of the output:
it's like creating dal and rice parallely and serving them together.