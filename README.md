# PDF RAG QA System 📄🤖

A **Retrieval-Augmented Generation (RAG)** system that processes research papers, stores their semantic representations in a vector database, retrieves relevant content, and generates answers using **Google Gemini**.

The project is implemented as a **Jupyter Notebook-based RAG pipeline** and uses research papers as the knowledge source.

## 🚀 Features

* 📄 Load research papers from PDF files
* 🔍 Extract text from PDFs using **PyMuPDF**
* 🧹 Clean and preprocess extracted text
* ✂️ Split documents into smaller chunks
* 🏷️ Maintain document metadata
* 🧠 Generate embeddings using **Google Gemini**
* 🗄️ Store embeddings in **ChromaDB**
* 🔎 Retrieve relevant chunks using similarity search
* 🤖 Generate context-aware answers using **Google Gemini**
* 📚 Use multiple research papers as the knowledge base

## 🔄 RAG Workflow

```text
Research Paper PDFs
        ↓
   Text Extraction
     (PyMuPDF)
        ↓
 Text Cleaning & Processing
        ↓
    Text Chunking
        ↓
 Gemini Embeddings
        ↓
     ChromaDB
   Vector Database
        ↓
   Similarity Search
        ↓
 Relevant Text Chunks
        ↓
   Google Gemini
        ↓
     Final Answer
```

## 🛠️ Tech Stack

| Technology       | Purpose                              |
| ---------------- | ------------------------------------ |
| Python 3.11      | Development                          |
| Google Gemini    | Embeddings & answer generation       |
| ChromaDB         | Vector storage and similarity search |
| PyMuPDF          | PDF text extraction                  |
| NumPy            | Data processing                      |
| Pandas           | Data handling                        |
| python-dotenv    | Environment variable management      |
| Jupyter Notebook | Development and experimentation      |

## 📁 Project Structure

```text
PDF_RAG_QA_SYSTEM/
│
├── data/
│   └── pdfs/
│       ├── Researchpaper1.pdf
│       └── Researchpaper2.pdf
│
│
├── academic_research_project.ipynb
├── pyproject.toml
├── requirements.txt
├── uv.lock
├── .python-version
├── .gitignore
└── README.md
```

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone https://github.com/Moni-5/PDF-RAG-QA-System.git
cd PDF-RAG-QA-System
```

### 2. Create the environment

The project uses Python 3.11.

Using `uv`:

```bash
uv venv
```

Activate the environment on Windows:

```powershell
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
uv pip install -r requirements.txt
```

### 4. Configure the API key

Create a `config.env` file in the project root:

```env
GOOGLE_API_KEY=your_google_gemini_api_key
```

The API key file is excluded from Git using `.gitignore`.

## ▶️ Running the Project

Open the Jupyter notebook:

```text
academic_research_project.ipynb
```

Run the notebook cells sequentially to:

1. Load the research papers
2. Extract and clean the PDF content
3. Split the content into chunks
4. Generate Gemini embeddings
5. Store embeddings in ChromaDB
6. Perform similarity-based retrieval
7. Generate answers using Gemini

## 🧠 How RAG Works in This Project

Instead of asking the language model to answer directly from its general knowledge, the system first searches the research papers for relevant information.

The retrieved document chunks are then provided as context to Gemini, allowing the model to generate an answer grounded in the retrieved research content.

This follows the basic RAG pattern:

```text
Query
  ↓
Embedding / Retrieval
  ↓
Relevant Document Chunks
  ↓
Context + Query
  ↓
Gemini
  ↓
Generated Answer
```

## 🔐 Security

* API credentials are stored in `config.env`
* `config.env` is excluded through `.gitignore`
* API keys should never be committed to GitHub

## 📌 Project Scope

This project is a **notebook-based RAG prototype** focused on document ingestion, vector retrieval, and question answering over research papers.

Possible future improvements include:

* Web-based user interface
* PDF upload functionality
* Persistent vector database
* Source and page-number references
* Multiple document collections
* Conversational chat history
* Improved retrieval and reranking

## 👨‍💻 Author

**Monish Allam**

GitHub: https://github.com/Moni-5
