# First Aid RAG Chatbot

A Retrieval-Augmented Generation (RAG) based command-line chatbot built with LangChain, ChromaDB, and Google Gemini. It answers first aid questions by retrieving context directly from a local directory of medical guidelines, reducing the risk of LLM hallucinations. 

**Note:** This is a portfolio project built for educational purposes. It is not a substitute for professional medical advice. Always call local emergency services in a real medical emergency.

## Overview

I built this project to experiment with local vector stores and context-grounded LLM responses. Instead of relying on Gemini's base training data, the bot is forced to cite and answer from a provided set of first-aid markdown files.

**Core features:**
* Uses **ChromaDB** to locally index and search custom first-aid manuals.
* Uses LangChain's `RecursiveCharacterTextSplitter` to chunk documents while preserving context overlap.
* Includes a custom caching mechanism for vector embeddings to avoid redundant Gemini API calls on startup.
* Runs as a continuous interactive CLI loop.

## Tech Stack
* **Python**
* **LangChain** (Core framework, chunking, retrieval chains)
* **Google Gemini Pro** (LLM & Embeddings API)
* **ChromaDB** (Vector Database)

## Running the Project

### Prerequisites
You will need a Google account (if running in Colab) and a free [Google Gemini API key](https://makersuite.google.com/app/apikey).

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Araf-Tahsan/First-Aid-RAG-Assistant.git
   cd First-Aid-RAG-Assistant
