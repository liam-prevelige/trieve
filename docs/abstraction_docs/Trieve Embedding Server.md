# Trieve Embedding Server

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
30["<b>Trieve Embedding Server</b><br/><small>abstraction_docs</small>"]:::mainNode

```

## Core Functionality
- **Embedding Generation**:
  - `main.py`: Sets up a FastAPI application to generate embeddings using a pre-trained model from the Hugging Face Transformers library.
