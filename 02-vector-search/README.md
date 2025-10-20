# Vector Search - RAG Implementation

RAG (Retrieval-Augmented Generation) implementation using Hugging Face models and vector search.

## Setup

**Prerequisites:**
- Hugging Face API token (stored in `.env` file in project root)
- Docker (for Qdrant vector database)

**Start Qdrant:**
```bash
docker run -d -p 6333:6333 -p 6334:6334 \
   -v "./qdrant_storage:/qdrant/storage:z" \
   qdrant/qdrant
```

## Notebooks

1. **01_sematic_search.ipynb** - Vector search fundamentals with Qdrant
2. **02_rag-starter.ipynb** - Basic RAG with text search (Minsearch)
3. **03_rag.ipynb** - Advanced RAG with vector search (Qdrant)
4. **04_hybrid_search.ipynb** - Hybrid search (BM25 + Dense vectors)

## Tech Stack

- **LLM**: Meta Llama-3.2-3B-Instruct (via Hugging Face Inference API)
- **Embeddings**: Jina Embeddings v2 Small (512-dim)
- **Vector DB**: Qdrant
- **Framework**: LangChain
