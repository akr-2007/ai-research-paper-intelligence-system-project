# AI Research Paper Intelligence System

### Semantic Search & AI-Powered Research Summarization using Sentence Transformers, FAISS, and T5

## Overview

Finding relevant research papers from thousands of publications can be time-consuming and inefficient when relying solely on keyword-based search.

This project develops an AI-powered Research Paper Intelligence System that leverages semantic search and transformer models to retrieve relevant research papers based on meaning rather than exact keywords. The retrieved papers are further summarized into concise research briefs using an abstractive text summarization model.

The system demonstrates an end-to-end NLP pipeline integrating semantic embeddings, vector search, and transformer-based summarization.

---

## Problem Statement

Traditional keyword search often fails to capture the true semantic intent of user queries.

The objective of this project is to build an intelligent research assistant capable of:

* Understanding semantic meaning behind user queries.
* Retrieving the most relevant research papers.
* Generating concise AI-powered summaries.
* Improving research discovery and literature review efficiency.

---

## Dataset

**Dataset:** ML-ArXiv Papers Dataset (Hugging Face)

The dataset contains Machine Learning research papers including:

* Paper Title
* Abstract

Approximately 15,000 research papers were processed.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Hugging Face Datasets
* Sentence Transformers
* FAISS
* Transformers (T5)
* PyTorch

---

## Project Workflow

### 1. Dataset Preparation

* Loaded the ML-ArXiv dataset.
* Selected titles and abstracts.
* Combined both into a unified text representation.
* Cleaned formatting issues and whitespace.
* Processed 15,000 research papers.

---

### 2. Semantic Embedding Generation

Generated dense vector representations using:

**Sentence Transformer**

* all-MiniLM-L6-v2

Each research paper was converted into a semantic embedding that captures contextual meaning rather than relying on exact keyword matches.

---

### 3. Vector Database Construction

Implemented FAISS (Facebook AI Similarity Search) to build a high-performance vector index.

Steps included:

* L2 normalization of embeddings.
* Building an IndexFlatIP similarity index.
* Efficient nearest-neighbor retrieval.

---

### 4. Semantic Search

The search pipeline:

1. Convert user query into an embedding.
2. Normalize the query vector.
3. Search the FAISS index.
4. Retrieve the most semantically similar research papers.
5. Display similarity scores and abstract previews.

Unlike traditional search engines, retrieval is based on contextual similarity rather than exact keyword matching.

---

### 5. AI-Powered Summarization

Integrated the T5-small Transformer model to automatically summarize retrieved research papers.

The generated summaries provide concise research briefs, helping users quickly understand the core contributions of each paper.

---

## Features

* Semantic research paper search
* AI-generated research summaries
* Fast vector similarity search
* Transformer-based NLP pipeline
* Efficient handling of large document collections
* Modular and scalable architecture

---

## Applications

This system can be used for:

* Academic research
* Literature review
* Research recommendation systems
* Knowledge discovery
* AI-powered digital libraries
* Enterprise document retrieval

---

## Future Improvements

* Retrieval-Augmented Generation (RAG) with Large Language Models
* Interactive Streamlit or Flask web application
* Hybrid keyword + semantic search
* Metadata filtering by author, year, or category
* PDF ingestion and document indexing
* Conversational research assistant with citation support

---

## Conclusion

This project demonstrates an end-to-end AI-powered information retrieval system by combining Sentence Transformers for semantic embeddings, FAISS for efficient vector search, and the T5 Transformer for abstractive text summarization.

The integration of semantic search with AI-generated summaries enables users to discover relevant research efficiently and quickly understand key insights, showcasing the practical application of modern NLP and information retrieval techniques.
