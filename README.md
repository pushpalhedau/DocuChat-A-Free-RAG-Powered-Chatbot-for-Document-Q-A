# DocuChat-A-Free-RAG-Powered-Chatbot-for-Document-Q-A

I developed a Retrieval-Augmented Generation (RAG) chatbot that combines traditional information retrieval with the power of generative language models to provide accurate, context-aware answers based on custom text data.

Key Components and Workflow:
1. Document Parsing and Chunking with LangChain
Using LangChain, I parsed and chunked input documents into manageable text segments. This chunking process ensures that each piece of text is of optimal length for embedding and retrieval, improving the relevance of search results during inference. LangChain also provided a modular and extensible framework for integrating different components of the RAG architecture.

2. Semantic Search via Vector Embeddings
To enable semantic search:

I used sentence-transformers with the MiniLM model to convert each document chunk into a high-dimensional embedding vector that captures the semantic meaning of the text.

These vectors were stored in a FAISS (Facebook AI Similarity Search) index, a fast and efficient library for similarity search over dense vectors. This allows for quick retrieval of the most relevant chunks based on user queries.

3. Answer Generation with FLAN-T5
For generating responses:

I integrated FLAN-T5, an open-source, instruction-tuned language model from Hugging Face. FLAN-T5 was chosen for its strong performance on general QA tasks and its open-access nature.

Retrieved text chunks were passed along with the user query to FLAN-T5, enabling it to generate context-aware, informative responses grounded in the source documents.

4. Interactive Deployment via Gradio on Google Colab
The entire chatbot system was deployed using Gradio, which provides an easy-to-use web interface for interacting with the model.

I hosted the application on Google Colab, allowing for a free, browser-accessible environment to test and demonstrate the chatbot.

# Screenshot of the Project:

![Screenshot 2025-06-19 121051](https://github.com/user-attachments/assets/1dcc417a-d240-4a16-9d35-259f4fd9068a)
