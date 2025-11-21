**RAG system**

**Prerequisites**
- Sentence Embedding model used all-mpnet-base-v2
- LLM used google/gemma-2b-it (Get hugging face token )

Note: All models, chunking algorithm can be replaced with others

**Injestion:**
- Reads pdf pages
- Chunks the pages
- Converts to embeddings
- Save embeddings to vector database (Used pgvector extension of postgres)

**RAG pipeline:**
- Convert user query to embeddings
- Retrieve relevant embeddings based on cosine similarity
- Enhance/Augment relevant data with prompt
- Use LLM to generate answer from the grounded facts from pdf

**Improvements**
- Use Quantization (if hardware supports)
- Analyze RAG metrics
    - Ground Truth
    - Specific
    - Relevant chunks
    - All chunks
- others
