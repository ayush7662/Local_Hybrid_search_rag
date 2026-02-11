<h1 align="center">🖥️ Local RAG App with Hybrid Search </h1>

### A powerful document Q&A application that leverages Hybrid Search (RAG) and local LLMs for comprehensive answers. Built with RAGLite for robust document processing and retrieval, and Streamlit for an intuitive chat interface, this system combines document-specific knowledge with local LLM capabilities to deliver accurate and contextual responses.

## Quick Start

## LLM Model
bartowski/Llama-3.2-3B-Instruct-GGUF/Llama-3.2-3B-Instruct-Q4_K_M.gguf@4096

## Embedder Model
lm-kit/bge-m3-gguf/bge-m3-Q4_K_M.gguf@1024

## Features

### Local LLM Integration:

Uses llama-cpp-python models for local inference
Supports various quantization formats (Q4_K_M recommended)
Configurable context window sizes


### Document Processing:

PDF document upload and processing
Automatic text chunking and embedding
Hybrid search combining semantic and keyword matching
Reranking for better context selection


### Multi-Model Integration:

Local LLM for text generation (e.g., Llama-3.2-3B-Instruct)
Local embeddings using BGE models
FlashRank for local reranking.


## Install spaCy Model

pip install https://github.com/explosion/spacy-models/releases/download/xx_sent_ud_sm-3.7.0/xx_sent_ud_sm-3.7.0-py3-none-any.whl


## ⚡ Install Accelerated llama-cpp-python

### Windows (CPU)

pip install llama-cpp-python


## Create virtual environment:

py -3.11 -m venv venv

venv\Scripts\activate

## Install Dependencies:

pip install -r requirements.txt

## Model Setup

RAGLite extends LiteLLM with support for llama.cpp models using llama-cpp-python. To select a llama.cpp model (e.g., from bartowski's collection), use a model identifier of the form "llama-cpp-python/<hugging_face_repo_id>/@<n_ctx>", where n_ctx is an optional parameter that specifies the context size of the model.

1. LLM Model Path Format:

llama-cpp-python/<repo>/<model>/<filename>@<context_length>

Example:

bartowski/Llama-3.2-3B-Instruct-GGUF/Llama-3.2-3B-Instruct-Q4_K_M.gguf@4096

2.Embedder Model Path Format:

llama-cpp-python/<repo>/<model>/<filename>@<dimension>

Example::

lm-kit/bge-m3-gguf/bge-m3-Q4_K_M.gguf@1024


## Database Setup

The application supports multiple database backends:

PostgreSQL (Recommended):

Create a free serverless PostgreSQL database at Neon in a few clicks

Get instant provisioning and scale-to-zero capability

Connection string format: postgresql://user:pass@ep-xyz.region.aws.neon.tech/dbname


## How to Run

1. Start the Application:

streamlit run local_main.py


2. Configure the Application:

Enter LLM model path

Enter embedder model path

Set database URL

Click "Save Configuration"

3. Upload Documents:

Upload PDF files through the interface

Wait for processing completion

4. Start Chatting:

Ask questions about your documents

Get responses using local LLM

Fallback to general knowledge when needed






















