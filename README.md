## RAG system

### Prerequisites
- Sentence Embedding model used all-mpnet-base-v2
- LLM used google/gemma-2b-it (Get hugging face token )

### Ingestion:
- Reads pdf pages
- Chunks the pages
- Converts to embeddings
- Save embeddings to vector database (Used pgvector extension of postgres)

### RAG pipeline:
- Convert user query to embeddings
- Retrieve relevant embeddings based on cosine similarity
- Enhance/Augment relevant data with prompt
- Use LLM to generate answer from the grounded facts from pdf

### Improvements

- Analyze RAG metrics
    - Ground Truth -> Check cosine similarity between relevant chunks and answer
    - Specific -> Get feedback from client
    - Relevant chunks
    - All chunks
    - Ragas depends on openAI to judge scores

### Strategy - Explore various options like below
- Read document like pymupdf, docling (handles images, tables)
- Chunking like Recursive, fixed etc
- Embedding like all-mpnet-base-v2
- Open (like google/gemma-2b-it) and closed source(Openai) LLMs
- Vector indexes like pgvector, pinecone
- Quantization (if hardware supports) like 8 bit, 4 bit

