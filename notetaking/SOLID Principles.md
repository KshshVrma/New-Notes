S: single responsibility principle:
each class should follow a single responsibility as this promotes less couplling, so if the class needs to perform multiple task then create a new class...
bad eg; a class doing adduser and sendmail both.

Open closed principle:
the code shold be open to expansion but closed to modification .
bad eg , a payment system implemented as differnet types of payment in a if else structure, if a new type of payment has to be added in that scenario we have to modify the existing code , instead have a interface payment , with paymet types implementing the interface, so that if in future we add a new payment type then we can simply add a new class for that payment type.

Liskov substitution method:
subclasses should be replacable by their superclasses without breaking any functionality. eg instead of having an interface bird with method fly in thiat cases a penguin cannot be replaced by a bird, we can have two interfaces bird and flying bird, the flying bird could have a method fly, now sparrow can implement both bird and flying bird class and penguin can simply implement the bird class.

Interface Segregation principle:
the user must not be forced to implemnt methods of an interface if he does not want to use that methods, so the interfaces should be broken down in order to 

Dependency inversion principle
[[lld roadmap]]
