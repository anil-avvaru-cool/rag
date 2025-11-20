RAG system

Injestion:
Reads pdf pages
Chunks the pages
Converts to embeddings
Save embeddings to vector database (Used pgvector)

RAG:
Convert user query to embeddings
Retrieve relavent embeddings based on cosine similarity
Enchance/Augment relavent data with prompt
Use LLM to generate answer from the grounded facts from pdf
