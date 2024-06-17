# ChunkMetadataDisplay.tsx

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
3362171312["<b>ChunkMetadataDisplay.tsx</b><br/><small>search/src/components/</small>"]:::mainNode

```
### Purpose
The `ChunkMetadataDisplay` component is designed to display metadata and content related to a specific chunk of data. It provides various functionalities such as viewing images, PDFs, and metadata, as well as editing and deleting the chunk.

### Flow
1. **Imports and Setup**: The file imports necessary libraries and components, including Solid.js hooks, utility functions, and icons.
2. **Helper Functions**: 
   - `getLocalTime`: Converts a given date to local time.
3. **Component Props**: Defines the `ChunkMetadataDisplayProps` interface to specify the expected properties.
4. **Component Initialization**: 
   - Uses Solid.js signals to manage state (e.g., `expanded`, `deleting`, `deleted`).
   - Retrieves context data using `useContext`.
5. **Delete Functionality**: 
   - `onDelete`: Sets up the deletion process for the chunk, including API call and state updates.
6. **Memoized Values**: 
   - `imgInformation`: Extracts image range information from the chunk metadata.
   - `useExpand`: Determines if the chunk content should be expandable based on its length.
   - `currentOrgId`: Retrieves the current organization ID from the context.
7. **Rendering**:
   - Displays chunk metadata and content with various conditional elements.
   - Provides buttons for viewing images, PDFs, and full metadata.
   - Includes edit and delete options for authorized users.
   - Uses `Show` and `For` components to conditionally render elements based on state and props.
   - Sanitizes and displays HTML content of the chunk.
   - Handles expand/collapse functionality for long content.
8. **Modals**:
   - `FullScreenModal`: Displays images and full metadata in a modal when triggered.
```

##### Auto generated documentation file from CodeViz.ai
