# RAG-for-querying
Independent RAG pipeline

Pipeline includes:
1. Loading of JSON (data folder)
2. Semantic Chunking
   Using library and model: 
   from semantic_text_splitter import TextSplitter
   model = all-MiniLM-L6-v2
3. Embedding to Chroma DB (Vector Store)
   Using model = gpt-4o-mini
4. Using cosim (vector store similarity search to find top k[20] chunks with query)
5. Prompt llm to summarise and generate a final response using the top k chunks.
