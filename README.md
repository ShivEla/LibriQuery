
LibriQuery: Command-Line RAG Book Q&A System
Overview
LibriQuery is a Retrieval-Augmented Generation (RAG) system that answers your book-related questions directly from the command line. It combines the vast knowledge of Open Library APIs with the generative power of the Google Gemini LLM to deliver accurate and contextually rich responses. This pure Python script offers a straightforward way to interact with a sophisticated RAG system.

Features
Intelligent Q&A: Ask natural language questions about books (e.g., "What's the plot of 'Dune'?", "Who is Jane Austen?").

Comprehensive Data Retrieval: The system intelligently extracts search terms, then fetches and enriches book data from various Open Library APIs (including detailed descriptions, genres, author bios, publication specifics, and cover URLs).

Contextual Generation: Retrieved information grounds the Gemini LLM, ensuring factual and relevant answers, minimizing "hallucinations."

Command-Line Interface: Simple text-based interaction for quick queries and responses.

How It Works
You input a question.

Gemini extracts key search terms.

The system retrieves and enriches detailed book/author data from Open Library.

This rich data augments the prompt sent to Gemini.

Gemini generates a concise answer based on the provided context.

The answer is displayed in your terminal.
