[[Microservices]][[Google Kubernetes Engine]]
why for docker containers we need so small resources that for even a small machine can run 50 docker containers.

important terms related to docker:

docker image: 
this contains the information, ie the code and steps to run it? 
does it actually contain the entire code/ the libs that need to be installed. 

docker file:
this contains the steps that are run in the os kernal when we run docker build
this generates an docker image

docker container:
are the runtime execution of a docker image
eg a docker image contains instruction? of having linux os (Ubuntu) and sql server.
a running docker container would have a running instance of that docker image with a ubuntu and sql. docker engine is used to start a docker image and to convert it to docker container.


docker repository:
all the docker images are stored in docker repository and these repository expose rest endpoints which can be used to access the image. ie to it we can pull/push the docker images, in a repository there might be public and private images.

docker hub:
is a docker repository with access to all the public docker images, which can be pulled by anyone.




what does sandboxing mean?