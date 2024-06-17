# group_handler.rs

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
206922554["<b>group_handler.rs</b><br/><small>server/src/handlers/</small>"]:::mainNode

```
### Purpose
This file contains the implementation of various API endpoints for managing and interacting with chunk groups within a dataset. It includes functionalities for creating, updating, deleting, and retrieving chunk groups, as well as adding and removing chunks from groups. Additionally, it provides search and recommendation capabilities for chunk groups.

### Flow
1. **Dataset Ownership Check**:
   - `dataset_owns_group`: Verifies if a group belongs to a specific dataset using either a group ID or tracking ID.

2. **Create Chunk Group**:
   - `create_chunk_group`: Creates a new chunk group with optional metadata, tags, and tracking ID. Supports upsert functionality.

3. **Retrieve Groups**:
   - `get_specific_dataset_chunk_groups`: Fetches groups belonging to a specific dataset, paginated.
   - `get_group_by_tracking_id`: Retrieves a group using its tracking ID.
   - `get_chunk_group`: Retrieves a group using its group ID.

4. **Update Chunk Group**:
   - `update_group_by_tracking_id`: Updates a chunk group using its tracking ID.
   - `update_chunk_group`: Updates a chunk group using either its group ID or tracking ID.

5. **Delete Chunk Group**:
   - `delete_group_by_tracking_id`: Deletes a chunk group using its tracking ID, with an option to delete contained chunks.
   - `delete_chunk_group`: Deletes a chunk group using its group ID, with an option to delete contained chunks.

6. **Manage Chunks in Groups**:
   - `add_chunk_to_group`: Adds a chunk to a group using the group ID.
   - `add_chunk_to_group_by_tracking_id`: Adds a chunk to a group using the group's tracking ID.
   - `get_chunks_in_group`: Retrieves chunks within a group, paginated.
   - `get_chunks_in_group_by_tracking_id`: Retrieves chunks within a group using the group's tracking ID, paginated.
   - `remove_chunk_from_group`: Removes a chunk from a group.

7. **Search and Recommendations**:
   - `get_recommended_groups`: Provides recommendations for groups based on positive and negative group IDs or tracking IDs.
   - `search_within_group`: Searches for chunks within a specific group based on a query.
   - `search_over_groups`: Searches for groups based on a query, returning groups with matching chunks.

8. **Utility Functions**:
   - `parse_query`: Parses the search query for further processing.
   - `get_metadata_from_tracking_id_query`, `get_group_by_id_query`, `get_group_from_tracking_id_query`: Helper functions to fetch metadata and group details from the database.
   - `create_group_query`, `update_chunk_group_query`, `delete_group_by_id_query`: Database operations for creating, updating, and deleting groups.
   - `create_chunk_bookmark_query`, `delete_chunk_from_group_query`: Database operations for managing chunk bookmarks within groups.
   - `add_bookmark_to_qdrant_query`, `remove_bookmark_from_qdrant_query`: Operations for managing bookmarks in the Qdrant vector database.
   - `full_text_search_over_groups`, `hybrid_search_over_groups`, `semantic_search_over_groups`: Search operations over groups using different search strategies.
   - `get_metadata_from_groups`: Fetches metadata for groups from the database.
   - `recommend_qdrant_groups_query`: Fetches recommended groups from the Qdrant vector database.
```

##### Auto generated documentation file from CodeViz.ai
