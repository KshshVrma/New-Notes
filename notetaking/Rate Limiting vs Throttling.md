
Rate Limiting:

we do not want our systems to succumb under the pressure of a ton of request so, we limit the number of users which can access our systems.
the user which tries to access the system post the limit has been reached receives an error.


Throttling:

here we do not reject a request but place that in a queue.
(we might still throw an error if a upper limit threshold has been reached)
we can decide to:
process a constant number of request per unit time 
(like a leaking bucket which overflows at one point).

normally systems might decide to implement both throttling and rate limiting.