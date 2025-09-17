blue green deployments are a way to securely and reliable deploy any code to productions, here we transfer the traffic from blue to green system by flipping a switch, this can be done through a proxy or load balancer.

blue system: is the existing code,
green system is the new code,

suppose we want to deploy the new project version (green system)
, till we test for eg using automation testing , we maintain the old fleet of servers, so that if required we can easily rollback to the old deployemnt. This allows us to deploy the new build without any downtime, and it can even be done in the peak traffic hours.

key points:

have to maintain a different and identical number of servers so thus incurring double the cost
the deployments should be forward and backward compatible, as if for example we make a db change ie a columns type from string to int, then in that case suppose the green deployment fails , then if we revert to the old deployment then the old deployment will also fail

for stateful applicatons, this might cause an issue as if the data is being stored /cached by the servers, then we would loose the data while switching back from green to blue.

this is a good way to deploy any code, if you don't want any downtime and can afford double the infrastructure cost involved.

there has to be a good automation test setup so that validation of the green deployment can be validated quickly to reduce cost.

[[Canary Deployments]]