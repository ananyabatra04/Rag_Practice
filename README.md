This repository consists of my practice of RAG techniques. 

LLMs are trained on a fixed dataset, which limits their ability to handle private or recent information. They can sometimes "hallucinate", providing incorrect yet believable answers. Fine-tuning can help but can be expensive if we keep retraining on new data. Instead, the Retrieval-Augmented Generation (RAG) framework can help by using external documents to improve the LLM's responses through in-context learning. RAG ensures that the information provided by the LLM is not only contextually relevant but also accurate and up-to-date.

There are 4 main steps:
Indexing: Split the documents into chunks and embed them. These embeddings are then added to a vector store.
Retriever: Then, the retriever finds the most relevant documents based on the user's query, using techniques like vector similarity from the vector store.
Augment: After that, the Augment part combines the user's query with the retrieved context into a prompt, ensuring the LLM has the information needed to generate accurate responses.
Generate: Finally, the combined query and prompt are passed to the model, which then generates the final response to the user's query.
These components of RAG allow the model to access up-to-date, accurate information and generate responses based on external knowledge. However, to ensure RAG systems are functioning effectively, it’s essential to evaluate their performance.
