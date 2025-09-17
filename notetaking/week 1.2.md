for capacity estimation it is important to know the fundamentals correctly things that should be kept in mind is power of 2's till atleast 11/12 can be helpful , knowing the mapping between kb and mb and gb ie k*k=m, and m*  * k =g and g=10^30
some rules of thumb:
try to approximate each of the calculations for example 17k request day would translate to 17k/86400 better than that is using rounded of numbers ie 20 k and 100k, apart from this you can memorise some of the common mappings especially when it comes to millions so 1 million transactions in a day corresponds to roughly 12 transactions per second.

when it comes to scaling of the applications we need to ensure the design in a manner that the increase in capacity does not effect the performance there are 2 ways of scaling: increasing the capacity and then improving then improviing the efficiency of the code . when it comes to database when we opt for a sql data base we are preferring the acid properties ie the atomicity, consistency, durability , isolation over scalabilty because horizontally scaling a sql database is not easy although the sql database are normally very performant and can be scalled vertically the databases which are nosql are better for network partitioning and some of them are even build for it , when it comes to no sql we have column family: cassandra which can be partitioned by design, and document databases eg mongodb , which allow partition tolerance but not availabilty, it allows consistency though : in cap theorem we mainly check consistency ie if all the users are seeing the same data, availabilty can the user see the data incase of failures, and partition tolerance, ie how can the database handly network outage, etc.

first 150, then lld and then hld which is theoretical but needs to be practiced.

so today :
the are multiple possible implementaions of ai one could be making use of the Jira tickets and then scraping them and passing them to a llm inorder to get some categorization of the tickets done, which means that the ticket can be analyzed and few things could be done : like a summary of the ticket that is one use case, apart from that there could be resolutions which can be recommended by the llm and it could provide a summary of the steps to be followed to resolved, the issue the problem is that we may or may not be able to scrape the data entirely , one workaround could be to fnd the authentication token and making use of it to scrape the website, need to check if this would work for different page,s if it does, then what we can do is just scrape the data, pass the output to either some file so that it's output can be passed on to some llm and also the output can be written to some temporary file so that the data can be reused , so now the problem is broken into few parts, understnad if this is the best approach or there s something that s already existing for this scenario , so that the ai can be used to make judgements on top of a clearly filtered data, now once that is done, we can further optimize the outputs, and even feed the previous outputs as imputs as a sort of rag/finetuning the model to support out usecase, now as copilot alreay has access to out code base can we go a step ahead and combine the output of the first llm to be parsed as an input to the copilet which has some context and it can try to provide a meaning ful solution , i think for the hack it should be better if we try to assume that we are going to have that scraped data alrady present in some xml/json format to us which is ready to be used , it would be better if we can showcase something like this : challanges, if the tickets are huge we would need to chunk them so that we would be able to pass it as a input to the llm.
other than that we need to provide sufficient examples but now we should ensure that there are no hallucinations as this can actuallly be used by the developers especially useful for customer escalations.

// log hotel recommendation developer productivity, etc are some of the other use cases which can be taken up

for low level design there are some fundamental concepts that need to be mastered , which include, the conversion of a design or the requirements given by the user to a class diatgram so that the solution can be implemented
the points to be noted are the nouns should be conveted to classes and the verbs to their methods, 
the points to be taken care of is that while conversion we should take in to the account the relation ship between the classes , ie is it a is a relation or is it a has a relation if it is a is a relation it's most like going to be implemented usnig inheritence if it is a has a relation in that case it is just going to be it either a composition denoted by diamond symbol it means that one class cannot exist independently to the other class, and one example of this would be if we have a person and a credit card the card cnnot exist without the person , the other case would be cart and course where either can exist without the other and this would mean assosicaiton ;

When it comes to the single responsibility priciple in that case we, can assume that it should be in use by a single stakeholder so tha tif in future we do need to modify we are not breaking multiple flows.

Inheritance is about deciding which classes should be a part of the other class and top of that the methods that are required to be overriden so that we have a codebase that represents the reals lofe usercase and on top that it should be something that is maintainable in the sense that the lines of code should not be gigantic and it should be maintainable easily.

important intellij shortcuts include alt+1 and ctr+alt+left or right depending on the class that needs to be traversed. it is important to get to know about the experiences as well and on top of that, should have some hands on experience.

The ai model;s which are used for video generation generally make use of the concepts of diffusion and they depend upon transormers, so suppose if you have a input and then in multiple phases we pass on the outputs of the transformers to themselfes untill the output has gone through multiple cycles and the output is satisfactory , not only that it is similar to diffusion in physics in the sense that it moves towards more disorder? maybe.

declarative, pause, volume, warm-up, frameworks, one structure at a time

para:
point action result ask

3,2,1  on the spot
3 steps
2 types
1 thing

mastery cycle:
1. try and apply
2. reflect and review 
3. plan and improve

you can sound the way you want to..