# LangChain Fundamentals (Educational Guide)

This is a hands-on educational tutorial covering the core fundamentals of LangChain: chat models, prompt templates, LCEL, document loading, and text splitting.

---

## Files Included

- **`langchain.ipynb`**: The main notebook with interactive code and step-by-step explanations.
- **`article.txt`**: Sample text file used for text loading and chunking.
- **`Document_31.pdf`**: Sample PDF document used for document loader benchmarks.
- **`.env.example`**: Template for required API keys.

---

## How to Run Locally

### 1. Install Dependencies
```bash
pip install langchain langchain-anthropic langchain-google-genai pymupdf tiktoken python-dotenv
```

### 2. Set Up API Keys
Create your `.env` file from the example:
```bash
cp .env.example .env
```
Add your keys inside `.env`:
```env
ANTHROPIC_API_KEY=your_key_here
GEMINI_API_KEY=your_key_here
```

### 3. Open and Run
Open **`langchain.ipynb`** in VS Code or Jupyter Lab and run the cells sequentially.
