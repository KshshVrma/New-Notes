
gemini cli is a useful tool which if used correctly can have the context of the entire application, and be used to summarize entire text if required, 
not just this it is also capable to perform actions, if we compare the main 3 types of ai applicaiton one is rag: which is basically providing context to the llm to provide better solutions to the problem s, we create a vector database out of our documents, and then when the user prompts we fetch n most relevant embeddings from the vector database and then we use this to generate additional context that is used by the llm to provide more accurate answers.

mcp is basically model context protocol: what it does is basically combination of it being a client and there being multiple mcp servers, the client connects with the server not with rest but with sessions and uses it to perform actions, not just provide feedback which means that it can actually do something like book a hotel for you , which is going to be extremely useful in the future.

