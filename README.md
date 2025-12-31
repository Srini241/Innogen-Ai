# Innogen-Ai

## Description

RAG-based AI for startup–investor discovery using real, verifiable data.

## Project Setup

This project is built using a fully open-source stack designed for reliability and transparency. We use BAAI’s BGE embedding model to convert text into semantic vectors, ChromaDB to store and retrieve those vectors efficiently, and LLaMA as the large language model to generate final answers. The system runs locally or on a server, requires no paid APIs, and is easy to set up using Python with libraries like LangChain, BeautifulSoup, and pdfplumber. Once dependencies are installed, the project is ready to ingest data and respond to queries.

## Workflow

The workflow starts by collecting data from news articles, blogs, and PDF reports related to startups and venture capital. This raw data is converted into clean text, split into smaller chunks, and then transformed into embeddings using the BAAI model. These embeddings, along with their source metadata, are stored in ChromaDB. When a user asks a question, the same embedding model converts the query into a vector, ChromaDB retrieves the most relevant text chunks based on meaning, and LLaMA uses this retrieved context to generate an accurate, grounded response. This retrieval-first approach ensures the model does not hallucinate or invent information.

## Usage

Users can interact with the system by asking natural-language questions such as finding investors for a startup or identifying emerging trends in a specific sector. The system responds with concise answers that are based only on retrieved documents, making the output trustworthy and explainable. Because the pipeline is modular, new data sources can be added easily, and the language model or embeddings can be swapped if needed. Overall, the project acts like an AI research assistant that reads real documents first and answers only from verified data.
