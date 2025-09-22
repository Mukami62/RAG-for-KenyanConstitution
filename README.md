**RAG-for--KenyanConstitution**

This project builds a Retrieval-Augmented Generation (RAG) system using a Large Language Model (LLM) to answer questions about the Constitution of Kenya, 2010. The goal is to retrieve relevant articles from the Constitution PDF and provide clear, easy-to-understand explanations.

**Project Overview**

Downloaded and loaded the Constitution PDF using PDFMiner.

Split documents into chunks for embedding using a RecursiveCharacterTextSplitter.

Generated embeddings with HuggingFace (all-MiniLM-L6-v2) and stored them in a Chroma vector database.

Implemented a retrieval system to get the top 5 relevant document chunks for any question.

Built an LLM-based RAG chain using LLaMA 3.1 (via Groq) to generate natural-language answers.

Created a Python class (RAGApplication) for easy question answering.

**Methods Implemented**

Document preprocessing and chunking.

Vector embeddings and similarity search with Chroma.

Prompt design with LangChain’s PromptTemplate.

LLM generation with ChatGroq (LLaMA 3.1-8B instant).

RAG pipeline to combine retrieval and generation for accurate answers.

**Results**

Successfully retrieved relevant articles from the Constitution for example questions such as:

“What are grounds for losing a seat in a county assembly?”

“What are the rights of children under the Constitution?”

The system produces concise, beginner-friendly answers.

Retrieval ensures that the LLM answers are grounded in the actual Constitution text.

**Future Work**

Expand the RAG system to handle multiple versions of legal documents.

Improve prompt engineering for more detailed and structured answers.

Explore interactive web or mobile interfaces for easier question input.

Experiment with larger LLMs or fine-tuned legal models for more accurate answers.
