# RAG System

A Retrieval-Augmented Generation (RAG) application that lets you upload PDF documents and ask questions about them. Answers are grounded in the content of your documents instead of the model's general knowledge.

## How it works

1. **Chunking:** an uploaded document is split into small, overlapping text chunks so each one stays focused on a single idea.
2. **Embedding:** each chunk is converted into a vector (a list of numbers) that represents its meaning, and stored.
3. **Similarity search:** when you ask a question, it is embedded the same way, and cosine similarity finds the stored chunks closest in meaning to the question.
4. **Answer generation:** the top matching chunks are passed to the language model as context, which writes an answer based on them.

## Repositories

| Service | Repo | Stack | Role |
|---|---|---|---|
| API | [rag-api](https://github.com/Pramod0152/rag-api) | NestJS, TypeScript | Upload, orchestration, REST API |
| Web | [rag-web](https://github.com/Pramod0152/rag-web) | React | Chat interface |
| AI service | [rag-ai-service](https://github.com/Pramod0152/rag-ai-service) | Python, gRPC | Chunking, embeddings, retrieval |
