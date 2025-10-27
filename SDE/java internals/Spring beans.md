there are 3 ways to inject spring beans, especially in the old framework where we had to do a lot of wiring in that case we used xml based config files, some points to keep in mind:

we use a bean id to define a bean by default the beans are singleton however if there is a factory class that is normally used to create those beans then in that case
we should define that in the bean definintion in the xml file

the ways spring can inject those dependencies include constructor , setter and field out of these constructor is the most recommended for dependencies that ideally should be injected, we can provide names, and in spring boot to resolve name conflicts we can use the annotation which are qualifier and primary

when it comes to spring we make use of either applicationcontext or beanfactory to create and inject beans beanfactory creates beans based on the need basis, and applicationcontext creates all the beans right at the runtime. these normally are provided configuration xml files which means that the bean defined in those configuraion files will be loaded and injected by spring, 

these config files may include more imports of differnet config files, if imported form the libraries we can override them by manually adding those config files which are empty.

bean lifecycle:
bean creation is like leaf nodes are created first and we move up the order depending on the dependencies which are requrired to be injected, 

then the beans are injected

then we run the post construct methods 

then initializaiton

then we run the post initialization

bean ready to use

then we run the pre-cleanup methods 

and finally we delete the beans

ie:

Instantiation
    ↓
Populate Properties (DI)
    ↓
BeanNameAware / BeanFactoryAware
    ↓
BeanPostProcessor (before init)
    ↓
@PostConstruct / afterPropertiesSet / init-method
    ↓
BeanPostProcessor (after init)
    ↓
Bean Ready
    ↓
@PreDestroy / destroy-method