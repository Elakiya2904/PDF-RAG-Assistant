# 📄 PDF RAG Assistant

PDF RAG Assistant is a lightweight Retrieval-Augmented Generation (RAG) system that allows users to upload any PDF document and instantly query its content using natural language.  

The system extracts text from the PDF, breaks it into meaningful chunks, generates embeddings locally, and uses **FAISS** for efficient similarity search. When a user asks a question, the most relevant chunks are retrieved and passed to an LLM (**FLAN-T5**) to generate accurate, context-aware answers.

This project demonstrates the complete workflow of a RAG pipeline — including text extraction, chunking, embedding, vector indexing, retrieval, and generation — all running locally without external APIs. It is simple, fast, and ideal for building intelligent document-questioning systems for research papers, reports, manuals, or business documents.

---

## 🚀 Features
- 📄 PDF Upload Support  
- 🔍 Automatic Text Extraction & Chunking  
- 🧠 Local Embeddings (SentenceTransformers)  
- ⚡ FAISS Vector Search for retrieval  
- 🤖 LLM-based Answer Generation using FLAN-T5  
- 🖥️ Interactive Notebook UI (ipywidgets)  
- 🧹 Fallback response when answer is not found  

---

## 🛠 Tech Stack
- **Python 3**
- **PyPDF2** – PDF text extraction  
- **SentenceTransformers** – Embedding model  
- **FAISS** – Vector similarity search  
- **Transformers (FLAN-T5)** – LLM for answering  
- **Jupyter + ipywidgets** – Interactive UI  

---

## 📂 How It Works
1. User uploads a PDF.  
2. Text is extracted and split into overlapping chunks.  
3. Each chunk is embedded using **MiniLM**.  
4. **FAISS** builds an index of embeddings.  
5. On any user question:  
   - The system retrieves top-matching chunks.  
   - Sends them as context to **FLAN-T5**.  
   - Returns a concise answer.  

---
## ☁️ Run in Google Colab
```bash
# Open Google Colab in your browser
https://colab.research.google.com/

# Create a new notebook or upload the provided notebook file
pdf_rag_assistant.ipynb




# Install dependencies
pip install -r requirements.txt
