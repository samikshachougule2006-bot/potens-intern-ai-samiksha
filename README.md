# Document Q&A with Citations using RAG

## Potens AI/ML Internship Assignment 2026

### Overview

This project implements a Retrieval-Augmented Generation (RAG) system that answers questions from HR policy documents using Google Gemini and ChromaDB.

The system retrieves only the most relevant document chunks before generating an answer, reducing hallucinations and ensuring that responses remain grounded in the provided documents.

---

## Features

- Document ingestion from PDF files
- Recursive text chunking
- Semantic embeddings using Gemini Embedding Model
- Vector database using ChromaDB
- Question Answering with citations
- Document contradiction detection
- Multilingual querying
- Confidence score based on retrieval similarity
- Explicit handling of unknown questions

---

## Documents Used

- Attendance Policy
- Leave Policy
- Employee Handbook
- Work From Home Policy
- Code of Conduct

---

## Chunking Strategy

The documents were split using RecursiveCharacterTextSplitter.

Chunk Size: 500 characters

Chunk Overlap: 100 characters

This overlap preserves context between adjacent chunks while maintaining efficient retrieval.

---

## Technologies

- Python
- Google Gemini API
- ChromaDB
- LangChain
- Google Colab

---

## Project Workflow

PDF Documents

↓

Chunking

↓

Gemini Embeddings

↓

ChromaDB

↓

Similarity Retrieval

↓

Gemini Answer Generation

↓

Answer + Citations

---

## Implemented Features

### Ask Question

Returns:

- Answer
- Citations
- Confidence Score

### Contradiction Detection

Compares two documents and identifies conflicting statements with supporting evidence.

### Multilingual Support

Queries can be asked in multiple languages (tested with English and Marathi). Responses are generated in the same language while remaining grounded in the English source documents.

---

## How to Run

Open the notebook:

Potens_RAG_Project.ipynb

Run all cells sequentially.

Add your Gemini API key before running.

---

## Limitations

- Developed and validated in Google Colab.
- Uses a small HR policy document collection for demonstration.
- Confidence is based on vector similarity rather than model certainty.

---

## Future Work

- Streamlit interface
- FastAPI endpoints
- Persistent deployment
- Reranking
- Human-in-the-loop verification

---

## Author

Samiksha Chougule
