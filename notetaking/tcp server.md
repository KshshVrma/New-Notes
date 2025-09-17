a tcp server mainly contains some methods like listen, accept, read, write close...
the read and write calls are blocking calls,
so the server waits for client to send a request, however if the execution of the main logic requires a long period of time in that scenario then any second request if comes, will be accepted only post the first request is completely executed. so as a solution:


Why multiple threads are required:
we can have multiple thread and the new client request can be handled by the new thread, mean wihle if the old request is complete the old thread can accept any new request.