types of failure
problem with storing all request
solution: idempotent keys

Types of failure:
	any payment request can fail in 3 possible ways, in a client and server architecture, 
	1. it leaves the client but does not reach the server
	2. the server could not process the request.
	3. the server send back the request but the client hasn't received it yet.
now the client cannot retry payment in the scenarios, 2 and 3 and it cannot know which out of the 3 scenarios occur.

if it randomly retries the payment , in that scenario the transaction might occur multiple times, which is not desired.

therefor we need to ensure that server executes the transaction request only once

Problem with Storing all request:
	now one way to achieve idempotency is to store all possible request, and map if it has executed the request.. however this would be a more complicated solution and it would require storing and computing a lot of data, which would cause latency increase.

Solution Idempotent keys:
	so by design if the client send a random number associated with the transaction , the server can store that number and check if that transaction has occur or not, 
		now if the client wants to retry payment, in that case it can resend the request with that same random number. and the server will ensure that it will proceed only if the number hasn't been marked as done.
		
[[ACID props]]