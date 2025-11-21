**RAG system**

**Prerequisites**
- Sentence Embedding model used all-mpnet-base-v2
- LLM used google/gemma-2b-it (Get hugging face token )

Note: All models, chunking algorithon can be replaced with others

**Injestion:**
- Reads pdf pages
- Chunks the pages
- Converts to embeddings
- Save embeddings to vector database (Used pgvector extension of postgress)

**RAG pipeline:**
- Convert user query to embeddings
- Retrieve relavent embeddings based on cosine similarity
- Enchance/Augment relavent data with prompt
- Use LLM to generate answer from the grounded facts from pdf

**Improvements**
- Use Qunatization
- others
