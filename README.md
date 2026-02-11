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





