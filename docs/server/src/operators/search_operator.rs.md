# search_operator.rs

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
3391766847["<b>search_operator.rs</b><br/><small>server/src/operators/</small>"]:::mainNode

```
### Purpose
This file contains various functions and structures to handle search operations over chunks and groups of data. It integrates with Qdrant for vector-based searches and PostgreSQL for metadata retrieval and filtering. The file supports semantic, full-text, and hybrid search methods, as well as reranking and autocomplete functionalities.

### Flow
1. **Imports and Dependencies**: The file imports various modules and dependencies required for database operations, web handling, and Qdrant integration.

2. **Data Structures**:
   - `SearchResult`, `SearchChunkQueryResult`, `GroupScoreChunk`, `SearchOverGroupsResults`, etc., are defined to structure the search results and queries.

3. **Helper Functions**:
   - `convert_group_tracking_ids_to_group_ids`: Converts group tracking IDs to group IDs.
   - `get_qdrant_ids_from_condition`: Retrieves Qdrant IDs based on given conditions.
   - `assemble_qdrant_filter`: Assembles a Qdrant filter based on provided conditions and filters.
   - `get_metadata_filter_condition`, `get_group_metadata_filter_condition`, `get_group_tag_set_filter_condition`: Generate metadata filter conditions for Qdrant queries.

4. **Main Functions**:
   - `retrieve_qdrant_points_query`: Retrieves points from Qdrant based on search queries.
   - `retrieve_chunks_from_point_ids`: Retrieves chunk metadata from point IDs.
   - `rerank_chunks`: Reranks chunks based on recency, tag weights, and other criteria.
   - `search_semantic_chunks`, `search_full_text_chunks`, `search_hybrid_chunks`: Perform semantic, full-text, and hybrid searches over chunks.
   - `search_semantic_groups`, `search_full_text_groups`, `search_hybrid_groups`: Perform semantic, full-text, and hybrid searches within groups.
   - `semantic_search_over_groups`, `full_text_search_over_groups`, `hybrid_search_over_groups`: Perform semantic, full-text, and hybrid searches over groups.
   - `autocomplete_semantic_chunks`, `autocomplete_fulltext_chunks`: Provide autocomplete functionality for semantic and full-text searches.

5. **Qdrant Integration**:
   - Functions like `get_qdrant_connection`, `search_qdrant_query`, and `search_over_groups_query` handle the interaction with Qdrant for vector-based searches.

6. **Error Handling**:
   - The file includes error handling mechanisms to manage various failure scenarios, such as missing conditions or failed database operations.

7. **Tracing and Logging**:
   - The file uses tracing and logging to monitor the execution flow and capture errors for debugging and performance analysis.

##### Auto generated documentation file from CodeViz.ai
