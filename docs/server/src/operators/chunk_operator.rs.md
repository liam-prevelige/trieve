# chunk_operator.rs

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
165342132["<b>chunk_operator.rs</b><br/><small>server/src/operators/</small>"]:::mainNode

```
### Purpose
This file contains various asynchronous functions for handling chunk metadata operations in a database. These operations include fetching, inserting, updating, and deleting chunk metadata, as well as handling chunk collisions and managing group associations.

### Flow
1. **Fetching Metadata**:
   - `get_chunk_metadatas_from_point_ids`: Retrieves chunk metadata for given point IDs.
   - `get_slim_chunk_metadatas_from_point_ids`: Retrieves slim chunk metadata for given point IDs.
   - `get_point_ids_from_unified_chunk_ids`: Retrieves point IDs from unified chunk IDs.
   - `get_chunk_metadatas_and_collided_chunks_from_point_ids_query`: Retrieves chunk metadata and collided chunks for given point IDs.
   - `get_slim_chunks_from_point_ids_query`: Retrieves slim chunk metadata for given point IDs.
   - `get_content_chunk_from_point_ids_query`: Retrieves content chunk metadata for given point IDs.
   - `get_metadata_from_id_query`: Retrieves chunk metadata by chunk ID.
   - `get_metadata_from_tracking_id_query`: Retrieves chunk metadata by tracking ID.
   - `get_metadata_from_ids_query`: Retrieves chunk metadata for multiple chunk IDs.
   - `get_metadata_from_tracking_ids_query`: Retrieves chunk metadata for multiple tracking IDs.
   - `get_optional_metadata_from_tracking_id_query`: Retrieves optional chunk metadata by tracking ID.
   - `get_qdrant_id_from_chunk_id_query`: Retrieves Qdrant ID from chunk ID.
   - `get_qdrant_ids_from_chunk_ids_query`: Retrieves Qdrant IDs from chunk IDs.
   - `get_row_count_for_dataset_id_query`: Retrieves row count for a dataset ID.

2. **Inserting and Updating Metadata**:
   - `bulk_insert_chunk_metadata_query`: Bulk inserts chunk metadata.
   - `insert_chunk_metadata_query`: Inserts or updates chunk metadata.
   - `insert_duplicate_chunk_metadata_query`: Inserts duplicate chunk metadata.
   - `update_chunk_metadata_query`: Updates chunk metadata.

3. **Deleting Metadata**:
   - `delete_chunk_metadata_query`: Deletes chunk metadata and handles chunk collisions.
   - `bulk_revert_insert_chunk_metadata_query`: Reverts bulk insert of chunk metadata.

4. **Miscellaneous**:
   - `find_relevant_sentence`: Finds relevant sentences in chunk metadata based on a query.
   - `create_chunk_metadata`: Creates chunk metadata for bulk upload ingestion.
```

##### Auto generated documentation file from CodeViz.ai
