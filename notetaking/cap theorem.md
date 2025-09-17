[[RUM Conjecture]]

in any distributed data store:

can only provide the guarentees of 2 of the following three:
(in case of network partition failure, in order to achieve partition tolerance only one out of consistency or availability can be achieved.)

consistency:
every read must return the output from the most recent write or an error,
this is differnt from the definition of consistency of the acid.

availability:
every read must return atleast some response whether wrong or right.

partition tolerance:
given that the data is stored in an distributed manner, it should not fail even if a subpart of the network is disconnected from the other part of the network . eg network fault tolerance.

**this applies only to a system distributed over a wide area because over a single datacenter with enough good equipments you can almost guarentee that all 3 parts of the cap theorem be achieved.
