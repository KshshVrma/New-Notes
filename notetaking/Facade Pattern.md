[[Decorator Pattern]]

structural pattern.

This is a pattern which abstracts the usage of api's by the client for example in a reverse proxy we abstract the implementaton of the backend , 

even here we create a facade which simplifies the creation of the api's and this allowe the user/cleint to call just a single class/service to do all the functionality, for example the cline tdoes not have to call the paymentservice, userservice and orderservice classes to call their metods, they can just call the apigateway class , which will internally call all the required services and therefore clas all the functionalities by it;s own withtotu the user having to manually call the above classes by its own, 

this allows all the logic of authenticaion and security to be handled in the apigateway itself and we do not have to implemetn them individually for each of the services that we expose, this is an easier way to interact with microservicrs.