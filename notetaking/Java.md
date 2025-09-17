[[java streams]]

java is a object oriented based language : although is not completely object orited given the primitive type are present.. eg int, however there are wrappers around it namely Integer..

java has a relatively strong performace, and the benefit of java being htat even though it is not a scripting language, and need to be compiled first.. still the code and language is platform independent, which means that a code written in windows can be run in a mac machine.

this is mainly possible using the jvm..

jvm-> jre-> jdk;
       javac
java code-> byte code-> jvm(machine specific)-> machine code

so the java code is first compiled into byte code, now this byte code produced anywhere can be run in a diffent os using the jvm java virtual machine, as it is platform specific , and the jvam converts the code into output that can be understood by the operating system.

Jre is a combination of jvm and some runtime libraries so the common libraries that are required to be run in java are run and prsent in jre.

Jdk is the entire runtime environment including the compiler, jre and other items which are required to run jva program.

java is popular in the enterprise level applications because of it beigng supported by somuch documentation and developer tools : for setting up the application we have maven , ide like intellij which are mainly used for java development. also we have frameworks from java namely spring and spring boot.

howeever stil c++ is the best! because java is so versbose that it requires to be having a lot of abstraction . and for apparently for doing simple task a lot of boilerplate code is required , moreover it is much slower than cpp, and anyways we have languages which are speciallized todo other thing better than java,...
 the ui solution of java is jquirey an struts.. which is basically some login on top of mere html pages.. hwich is acutally used by entereprises.


in the future too we might have better alternatives like go, which will enfore the development of new java versions.

another speciality fo jva is the it has a built in garbage collector , which make the responsibiltiy of the developer lesser so that they don't have to mannully clall free everytime ensuring that the memorey of the heap remains intact and is somewhat dev freingdly in that direction.
					
Linkedlist<String> mylinkedlist = new Linkedlist<String>(); 2mylinkedlist. add("two"); 3myLinkedList.addFirst("one"); 4Iterator<String> iter = mylinkedlist.iterator();while (iter.hasNext()) { 6System.out.println(iter.next());  }

implement 3 stack with a array