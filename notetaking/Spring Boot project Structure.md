
spring boot comes with annotations by default, which are very useful as they allow the developer to autowire the classes and make use of different dependencies like the @repository class when extends a spring data jpa class then by default some of the methods are implemented to it which allows it to connect to the database without any extra configuration apart from specifying the details in application .properties.

the structure normally contains the following components:
(especially if following a mvc patter):

controller:
this component is mainly responsible for maintaining and definind the outputs and behaviors of endpoints, so the controllers ussually determine what happens when a user enters sometihning, ie if entering a endpoint which get request to triggerr fo the particular endpoint and so on.
the controller usually makes use of the service class for the business logic and refers to them when defining the function / routing the user from an endpoint.

Service:
this components mainly makes use of the different model classes / repository classes to define the main required business logic of the program, it contains the important function / method calls which would be made by the controller.

Model:
these are the entity classes which includes the interfaces and the clases that are used by the dao/ service classes , and tese basically contain the layout of the object as we are following object orientedl programming therefore the entity whih are present in the model component usually represents some real world object , these clases may extend other classes or implement any interface so as to make the project more extendible and follow the open close principle of the solid pricnliple.

Repository:
this component is mainly concerend about the database connections , and defining the sql / queryies along with making use of the entities of the model component.

[[Spring boot]]