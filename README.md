# Multimodal PDF RAG Assistant

A Retrieval-Augmented Generation (RAG) assistant that allows users to ask natural language questions about PDF documents. Unlike traditional PDF chatbots, this project extracts information from both textual content and images inside PDFs using OCR, generates semantic embeddings, retrieves the most relevant content, and uses a Large Language Model (LLM) to generate context-aware answers.

The project is implemented as a Jupyter Notebook and demonstrates an end-to-end multimodal RAG pipeline.

---

## Project Overview

The system performs the following steps:

1. Upload one or more PDF documents.
2. Extract text directly from PDF pages.
3. Extract images from each page.
4. Apply OCR on images using Tesseract.
5. Merge extracted text and OCR results.
6. Split the content into semantic chunks.
7. Generate embeddings using Sentence Transformers.
8. Store embeddings inside a FAISS vector database.
9. Retrieve the most relevant chunks for a user query.
10. Generate the final answer using a Large Language Model.

The overall goal is to improve question-answering performance for PDFs that contain both textual and image-based information.

---

## Features

- Text extraction from PDF documents
- OCR support for scanned PDFs and embedded images
- Multimodal document processing
- Semantic chunking
- Sentence Transformer embeddings
- FAISS vector similarity search
- Retrieval-Augmented Generation (RAG)
- Interactive notebook implementation
- Visualization support using UMAP
- Evaluation using ROUGE metrics

---

## Project Structure

```
.
├── Multimodal_PDF_RAG_Assistant.ipynb
├── sample_pdfs/
├── outputs/
├── README.md
```

The repository mainly consists of a Jupyter Notebook that contains the complete implementation of the pipeline.

---

## Technologies Used

### Programming Language

- Python 3

### Libraries

- pdfplumber
- pytesseract
- Pillow
- Sentence Transformers
- Transformers
- FAISS
- Gradio
- UMAP
- Matplotlib
- Scikit-learn
- ROUGE Score
- Joblib

### OCR Engine

- Tesseract OCR

### Vector Database

- FAISS

### Embedding Model

- Sentence Transformers

---

## Installation

Clone the repository.

```bash
git clone https://github.com/your-username/multimodal-pdf-rag-assistant.git

cd multimodal-pdf-rag-assistant
```

Install the required system packages.

### Ubuntu

```bash
sudo apt update

sudo apt install tesseract-ocr poppler-utils
```

### Windows

Install:

- Tesseract OCR
- Poppler for Windows

Add both installations to your system PATH.

---

## Python Dependencies

Install all required packages.

```bash
pip install --upgrade pip

pip install protobuf==3.20.3

pip install \
pdfplumber \
pytesseract \
pillow \
sentence-transformers \
transformers \
faiss-cpu \
gradio \
umap-learn \
matplotlib \
scikit-learn \
tabulate \
rouge-score \
joblib \
accelerate
```

---

## Running the Project

Open the notebook.

```bash
jupyter notebook
```

or

```bash
jupyter lab
```

Run every notebook cell sequentially.

The notebook will:

- install dependencies
- extract PDF content
- perform OCR
- create embeddings
- build the FAISS index
- retrieve relevant chunks
- generate answers

---

## Pipeline

```
PDF Documents
      │
      ▼
Text Extraction
      │
      ▼
Image Extraction
      │
      ▼
OCR using Tesseract
      │
      ▼
Combined Document
      │
      ▼
Chunking
      │
      ▼
Sentence Transformer Embeddings
      │
      ▼
FAISS Vector Database
      │
      ▼
User Query
      │
      ▼
Similarity Search
      │
      ▼
Retrieved Context
      │
      ▼
Large Language Model
      │
      ▼
Generated Answer
```

---

## Example Workflow

1. Upload a PDF.
2. The notebook extracts text from every page.
3. Images inside the PDF are extracted.
4. OCR converts image text into machine-readable text.
5. Text is divided into semantic chunks.
6. Embeddings are generated.
7. FAISS indexes all embeddings.
8. User enters a question.
9. Relevant chunks are retrieved.
10. The LLM generates the final response.

---

## Models Used

### OCR

Tesseract OCR

### Embedding Model

Sentence Transformers

### Retrieval

FAISS

### Language Model

Transformers-based LLM

---

## Evaluation

The notebook includes evaluation utilities such as:

- ROUGE Score
- Retrieval quality inspection
- Embedding visualization using UMAP

---

## Requirements

- Python 3.10+
- Jupyter Notebook
- Tesseract OCR
- Poppler Utilities

---

## Notes

- Scanned PDFs are supported through OCR.
- Text-based PDFs are processed directly.
- OCR results are merged with extracted text before indexing.
- FAISS enables efficient semantic retrieval even for large documents.

---

## Future Improvements

- Hybrid search (BM25 + Dense Retrieval)
- Metadata-aware retrieval
- Reranking models
- Support for multiple vector databases
- Support for multiple LLM providers
- Incremental indexing
- Web application deployment
- Multi-document collections
- Table extraction
- Figure caption understanding


## Author

Muhammad Hamza Nadeem
