we can make use of strategy + factory pattern:

service: factory of strategy to be used

interface strategy  and
implementatoins like upistrategy creditcardstrategy


the list can either be a enum or have a default payment strategy.

+-------------------------+
                |      PaymentService     |
                +-------------------------+
                | - factory: PaymentFactory|
                +-------------------------+
                | + process(request): void |
                +------------+-------------+
                             |
                             v
                +--------------------------+
                |     PaymentFactory        |
                +--------------------------+
                | + getStrategy(type):      |
                |       PaymentStrategy     |
                +------------+--------------+
                             |
        --------------------------------------------------
        |                                                |
        v                                                v
+------------------------+                +---------------------------+
|     PaymentStrategy    |<---------------|      UpiStrategy          |
+------------------------+   implements   +---------------------------+
| + pay(request): void   |                | + pay(request): void      |
+------------------------+                +---------------------------+

                                             ^
                                             |
                                             |
                              +---------------------------+
                              |   CreditCardStrategy      |
                              +---------------------------+
                              | + pay(request): void      |