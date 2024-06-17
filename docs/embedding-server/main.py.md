# main.py

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
375452138["<b>main.py</b><br/><small>embedding-server/</small>"]:::mainNode

```
### Purpose
This file sets up a FastAPI application to generate embeddings using a pre-trained model from the Hugging Face Transformers library. It provides an endpoint to process input text and return the corresponding embeddings.

### Flow
1. **Environment Setup**: Loads environment variables using `load_dotenv()`.
2. **Model Initialization**: Retrieves the model name from the environment and loads the pre-trained model with `AutoModel.from_pretrained()`.
3. **FastAPI Initialization**: Creates a FastAPI app instance.
4. **Data Models**: Defines Pydantic models for input (`OpenAIEmbeddingInput`) and output (`OpenAIEmbeddingResult`, `_EmbeddingObject`).
5. **Endpoint Definition**: 
   - Defines a POST endpoint `/embeddings`.
   - Accepts input as either a string or a list of strings.
   - Uses the model to generate embeddings.
   - Returns the embeddings in a structured JSON response.

##### Auto generated documentation file from CodeViz.ai
