# ChatBot-I-OpenAI-
## 📘 Workflow Overview

### 1. **Data Ingestion**
- Loads web-based documents using `WebBaseLoader`.
- Ingests content from: `https://docs.smith.langchain.com/`.

### 2. **Text Splitting**
- Uses `RecursiveCharacterTextSplitter` to divide documents into smaller chunks.
- Parameters: `chunk_size=500`, `chunk_overlap=20`.

### 3. **Embedding**
- Converts text chunks into numerical vectors using `OpenAIEmbeddings`.

### 4. **Vector Store (FAISS)**
- Stores and indexes embeddings using `FAISS`, an in-memory vector database.
- Enables fast similarity search.

### 5. **Retriever**
- Retrieves relevant chunks from FAISS based on semantic similarity to user queries.

### 6. **Document Chain**
- Constructs a prompt using retrieved documents and sends it to the LLM.
- Uses `create_stuff_documents_chain` with `ChatPromptTe_
