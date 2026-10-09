# LangChain & RAG Guide (Educational Tutorial)

A hands-on educational tutorial covering the fundamentals of LangChain, vector embeddings, vector databases (Qdrant), retrievers, and production RAG pipelines.

---

## Notebooks & Curriculum

- **`langchain.ipynb` (Part 1 - Fundamentals)**: Chat models (Anthropic & Gemini), message schemas, prompt templates, LCEL runnables, document loaders (PDF/Text), and text splitters.
- **`langchain_2.ipynb` (Part 2 - Vector Stores & RAG)**: HuggingFace embeddings (`all-MiniLM-L6-v2`), token limits inspection, Qdrant vector database, retrievers (Similarity, MMR), end-to-end RAG with source citations, streaming, and Pydantic structured outputs.

---

## Supporting Files

- **`article.txt`**: Sample text document used for text loading and chunking.
- **`Document_31.pdf`**: Sample PDF document used for document loader benchmarks.
- **`.env.example`**: Template for required API keys.

---

## How to Run Locally

### 1. Install Dependencies
```bash
pip install langchain langchain-anthropic langchain-google-genai langchain-qdrant sentence-transformers qdrant-client pymupdf tiktoken python-dotenv
```

### 2. Start Qdrant Vector Database (Required for Part 2)
```bash
docker run -p 6333:6333 qdrant/qdrant
```

### 3. Set Up API Keys
Create your `.env` file from the example:
```bash
cp .env.example .env
```
Add your keys inside `.env`:
```env
ANTHROPIC_API_KEY=your_key_here
GEMINI_API_KEY=your_key_here
```

### 4. Open and Run
Open **`langchain.ipynb`** (Part 1) or **`langchain_2.ipynb`** (Part 2) in VS Code or Jupyter Lab and run the cells sequentially.
