[[Adapter pattern]]
[[lld roadmap]]

(structural pattern)

this is a structural design pattern which allows us to extend the fuhnc tionalites of the classes without adding a ton of child classes which has been extended from a common parent on at a time, instead we create a decorator interface which implements the class, and this base decorator class is an abstract class which has the required class as the attribute and initialized it as a constructor , now all the new decorator classes which contain the new functionalityes can simply extend the base decorator class and extend the functionality of the class by using the constructor of the parent class to make use fo the objects in an neste way.

eg (Paneer(cheese(pizza))) here to the decorator of the paneer class we can just pass the object of the cheese pizza and the result would be a paneer cheese pizza , this is much better than normal implementation be cause if for example we had created a pizzqa class extended that with the cheese class, then extended that even with the pizzacheesepizza class then such a pattern would require 2^n classes, which is not feasable to be maintained ,thus instead we can just make use of the decorator pattern to add functionality on top of a class this just uses n classes and wastly simplifies the implemetation of ffunctionalities like this.

This allows the class to be independent of any order of procedure thus makes the implementation flexible and even modiyable at the runtime, which is a big plus point.
