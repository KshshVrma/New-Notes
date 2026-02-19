the different api's which are to be developed have to be agent friendly and as a consequence there are some of the things which we need to ensure that are correct:
whenever we are defining the api schemas in that scenario, ensure that the following are taken care:
semantic clarity which means that the endpoints are named properly, with proper endpoint description.
promptability and actionabilty; which means that the llm should be able to come up with the proper request object from the natural language text prompt without any failure, 
chainability: whetehr the llm can chain different operations which are performed which include the input of some of the api endpoints should clearly define the required parameters, like session id, definition of it should be clear so that the sequence of events is clear to the llm and the agent can perform chaining of the actions.
errror predictibiltiy basically defines how proper is the documentation for the error codes and if the description is clear or not which means that if the agent can successfully recover from errors or not.
schema clarity: if the datatypes which are present in the document are clear or not.
overall we generate the analysis along with the recommendation .

to build this we made use of adk web , which is a platform provided by google which allows development of agents, the model powering the agent was vertex ai provided by gcp.