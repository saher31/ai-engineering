# Qdrant: Vector Databases & Hybrid Retrieval

Practical implementations covering Qdrant vector database internals, sparse and dense vector representations, BM25, SPLADE, Hybrid Search, and two-stage Cross-Encoder re-ranking.

---

## Notebooks & Curriculum

- **`qdrant.ipynb` (Foundations & Vector Architectures)**:
  - Local Qdrant setup via Docker.
  - Dense vectors vs Sparse vectors (non-zero index and weight storage).
  - Inverted Index internals and `full_scan_threshold`.
  - BM25 lexical retrieval with FastEmbed and collection-wide `Modifier.IDF`.
  - SPLADE neural sparse models with automatic term expansion.

- **`hybrid_search.ipynb` (Hybrid Search & Re-ranking Pipeline)**:
  - Multi-vector collection setup (Dense + Sparse).
  - External dense encoding (`intfloat/multilingual-e5-small`) with `passage:` prefix.
  - Lexical sparse encoding (`Qdrant/bm25`) with document length calibration (`avg_len`).
  - Search evaluation across semantic, exact code, and mixed query types.
  - Reciprocal Rank Fusion (RRF) for combining dense and sparse results.
  - Two-stage retrieval: Re-ranking top candidates using `cross-encoder/ms-marco-MiniLM-L-6-v2`.

---

## Supporting Files

- **`support.txt`**: Customer support documentation dataset containing exact error codes, billing policies, and feature descriptions.

---

## How to Run Locally

### 1. Start Qdrant Vector Database
```bash
docker run -p 6333:6333 -p 6334:6334 qdrant/qdrant
```

### 2. Install Dependencies
```bash
pip install qdrant-client sentence-transformers fastembed
```

### 3. Run the Notebooks
Open `qdrant.ipynb` or `hybrid_search.ipynb` in your Jupyter environment and execute the cells sequentially.
