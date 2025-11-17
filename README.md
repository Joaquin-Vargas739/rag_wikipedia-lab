# rag_wikipedia-lab
This repository builds a retrieval-augmented summarization system using open-source Wikipedia data. It uses LangChain + ChromaDB + SentenceTransformers to query, embed, and summarize factual content from Wikipedia without multi-agent coordination.

# README.md — Task 2: RAG con Wikipedia

Joaquín — Perú  
17 nov 2025, 12:20 AM

¿Qué hace?
- Descarga Federated Learning de Wikipedia.
- Corta en pedazos (~300 palabras).
- Guarda en CSV y ChromaDB.
- Responde con Ollama (Mistral local).
- Genera:
  - rag_summary.md (400–500 palabras)
  - retrieval_examples.json

Archivos
notebooks/rag_wikipedia.ipynb
data/wiki_corpus.csv
outputs/rag_summary.md
outputs/retrieval_examples.json
requirements.txt

Requisitos
wikipedia-api
sentence-transformers
chromadb
langchain
transformers
torch
pandas
langchain-community
langchain-chroma

pip install -r requirements.txt

Ollama (obligatorio)
1. Descarga: ollama.com
2. Instala.
3. CMD como admin:
   ollama serve
4. Otra CMD:
   ollama pull mistral

Ejecutar
1. Abre rag_wikipedia.ipynb.
2. Corre todas las celdas.
3. Se generan los archivos en /outputs.

Entrega lista.
