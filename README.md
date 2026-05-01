# Simple RAG-Based Web Scraping with LangChain

A simple Retrieval-Augmented Generation (RAG) pipeline that scrapes a webpage, chunks the content, embeds it into a vector database, and uses an LLM to answer questions based on the scraped data.

This project demonstrates how to build a lightweight RAG workflow using:

- **LangChain**
- **OpenRouter / OpenAI-compatible LLMs**
- **HuggingFace Embeddings**
- **Chroma Vector Store**
- **Web Scraping via WebBaseLoader**

---

## Overview

This project scrapes content from a webpage (e.g. Walmart search results), converts the content into embeddings, stores it in a vector database, and enables natural language querying over the scraped data using a Retrieval-Augmented Generation (RAG) pipeline.

Example use case:

- Scrape product listings from an e-commerce website
- Store webpage content in a vector database
- Ask questions like:
  - *“Give me all products and prices in a table”*
  - *“Which products are under $50?”*
  - *“List the cheapest options available”*

---

## Workflow

1. **Scrape webpage content**  
   Load webpage content using LangChain’s `WebBaseLoader`.

2. **Split content into chunks**  
   Break large webpage text into smaller chunks for better retrieval.

3. **Generate embeddings**  
   Convert text chunks into vector embeddings using HuggingFace embeddings.

4. **Store in Chroma DB**  
   Save embeddings into a local Chroma vector database.

5. **Retrieve relevant chunks**  
   Query the vector store using semantic search.

6. **Generate final answer**  
   Use an LLM to answer questions based on retrieved context.

---

## Tech Stack

- **Python**
- **LangChain**
- **LangChain Community**
- **LangChain OpenAI**
- **ChromaDB**
- **HuggingFace Embeddings**
- **OpenRouter**
- **BeautifulSoup4**

---

## Project Structure

```bash
simple-rag-web-scraper/
│
├── Simple RAG based web scraping.ipynb   # Main notebook
├── requirements.txt                      # Dependencies
├── README.md                             # Project documentation
└── .env                                  # API keys (not committed)
