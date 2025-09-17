dummy release to production to check if all the deployments are correct and no usage spike is happening, 

if the deployment in for eg 1 server or a pod succeeds then the complete deployment is done to other servers, this is done to ensure that monitoring of the environment can happen , despite all the misses in the lower env by the qa and unit testing team.

rollbacks are faster