
**LibriQuery: Command-Line RAG Book Q&A System
**

This repository contains two distinct Python implementations of a Retrieval-Augmented Generation (RAG) system designed to answer questions about books. Both leverage Open Library APIs for data retrieval and Google Gemini models for natural language understanding and generation. They showcase different architectural approaches to building RAG applications.

**Features**
Intelligent Q&A: Ask natural language questions about books (e.g., "What's the plot of 'Dune'?", "Who is Jane Austen?").

Comprehensive Data Retrieval: The system intelligently extracts search terms, then fetches and enriches book data from various Open Library APIs (including detailed descriptions, genres, author bios, publication specifics, and cover URLs).

Contextual Generation: Retrieved information grounds the Gemini LLM, ensuring factual and relevant answers, minimizing "hallucinations."

Command-Line Interface: Simple text-based interaction for quick queries and responses.

_**LibriQuery: RAG Book Q&A System (LangChain/FAISS/Gemini):**_
This file presents a robust and modular RAG system built using the LangChain framework. It demonstrates a more advanced and structured approach to integrating external knowledge into an LLM's responses.

_RAG Architecture: _Employs a classic RAG pipeline with explicit components for retrieval and generation.

_Retrieval Mechanism: _Utilizes GoogleGenerativeAIEmbeddings to convert book content into numerical vectors. These vectors are stored and efficiently searched within an in-memory FAISS vector database. When a user asks a question, the system semantically searches this vector store to retrieve the most relevant book passages.

_LLM Integration: _Integrates the ChatGoogleGenerativeAI (using models like gemini-pro or gemini-1.5-flash) through LangChain's standardized interface.

_Context and Memory Management: _Leverages LangChain's ConversationalRetrievalChain and ConversationBufferMemory to automatically manage and inject both the retrieved context and the ongoing chat history into the LLM's prompts. This allows for seamless follow-up questions and a more natural conversational flow.

_Data Enrichment: _Includes helper functions to fetch detailed book information (descriptions, author bios, publication details, cover URLs) from various Open Library API endpoints, which are then used to populate the FAISS index.


_**Unified RAG Book Q&A System with Chat History :**_
This file provides a more direct and manual implementation of a RAG system, focusing on explicit API calls to Gemini and Open Library, with custom chat history management.
