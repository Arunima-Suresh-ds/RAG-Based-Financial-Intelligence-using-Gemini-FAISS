# RAG-Based-Financial-Intelligence-using-Gemini-FAISS
End-to-end Retrieval-Augmented Generation (RAG) system designed to enable intelligent question answering over financial documents. The project uses a financial PDF report (Sharekhan – Investor Eye) as the knowledge source and integrates Google Gemini with a FAISS vector database to generate accurate, context-aware responses.

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat&logo=python&logoColor=white)
![LLM](https://img.shields.io/badge/LLM-Google%20Gemini-673AB7)
![RAG](https://img.shields.io/badge/Technique-RAG-FF9800)
![VectorDB](https://img.shields.io/badge/Vector%20DB-FAISS-009688)
![Domain](https://img.shields.io/badge/Domain-Financial%20Documents-607D8B)
![Status](https://img.shields.io/badge/Status-Completed-2E7D32)


##  Project Overview
This project implements an **end-to-end Retrieval-Augmented Generation (RAG)** system using **Google Gemini**, **FAISS vector database**, and a **financial PDF document (Sharekhan – Investor Eye)**.  

The system allows users to ask natural language questions and receive **context-aware, accurate answers grounded in the source document**, overcoming the limitation of LLMs not having direct access to private or external documents.

---

##  Problem Statement
Financial reports are lengthy, complex, and time-consuming to analyze manually. Traditional LLMs may hallucinate or provide generic answers without understanding document-specific context.

**Objective:**  
Build a system that can:
- Understand financial PDFs
- Retrieve relevant information efficiently
- Generate precise, context-grounded answers

---

##  Solution Approach (RAG Pipeline)

1. **PDF Ingestion**
   - Load and extract text from the Sharekhan Investor Eye PDF using `PyPDF2`

2. **Text Chunking**
   - Split extracted text into smaller, semantically meaningful chunks

3. **Embedding Generation**
   - Convert text chunks into dense vector embeddings

4. **Vector Storage**
   - Store embeddings in a **FAISS** vector database for fast similarity search

5. **Query Processing**
   - Convert user queries into embeddings
   - Retrieve top-k relevant chunks from FAISS

6. **Answer Generation**
   - Pass retrieved context along with the user query to **Google Gemini**
   - Generate accurate, document-grounded responses

---

## Tech Stack

- **Language:** Python  
- **LLM:** Google Gemini  
- **Vector Database:** FAISS  
- **PDF Processing:** PyPDF2  
- **Embeddings:** LLM-based / Sentence embeddings  
- **Environment:** Jupyter Notebook  
