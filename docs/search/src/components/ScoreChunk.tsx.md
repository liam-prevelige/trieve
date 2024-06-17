# ScoreChunk.tsx

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
3078740785["<b>ScoreChunk.tsx</b><br/><small>search/src/components/</small>"]:::mainNode

```
### Purpose
The `ScoreChunk` component is designed to display and manage a chunk of data, including its metadata, images, and various actions such as viewing, copying, and deleting. It provides a detailed view of the chunk's content and associated metadata, along with user interactions for managing the chunk.

### Flow
1. **Imports and Context Setup**: The component imports necessary libraries and contexts, including Solid.js hooks, icons, and utility functions.
2. **Sanitizer Options**: Defines HTML sanitization options to ensure safe rendering of HTML content.
3. **Utility Functions**: Includes a `formatDate` function to format dates in `MM/DD/YYYY` format.
4. **Component Props**: Defines the `ScoreChunkProps` interface to specify the expected properties for the component.
5. **State Initialization**: Uses Solid.js signals to manage various states such as `expanded`, `showPropsModal`, `deleting`, `deleted`, `copied`, `showImageModal`, `showMetadata`, `expandMetadata`, `fileLink`, and `imageLink`.
6. **Effects**:
   - Fetches a signed URL for the file link if metadata contains the file name key.
   - Sets the image link if metadata contains image URLs.
   - Computes image information based on metadata keys.
   - Shows the properties modal if `showPropsModal` is true.
7. **Event Handlers**:
   - `deleteChunk`: Sets up the deletion process for the chunk.
   - `copyChunk`: Copies the chunk's HTML content to the clipboard.
8. **Memoized Values**:
   - `useExpand`: Determines if the chunk's HTML content should be expandable.
   - `currentUserRole`: Retrieves the current user's role.
   - `currentOrgId`: Retrieves the current organization ID.
9. **Rendering**:
   - Displays chunk information, including similarity score, tracking ID, tag set, time stamp, and location.
   - Provides buttons for viewing images, PDFs, metadata, copying content, deleting, and editing the chunk.
   - Renders the chunk's HTML content with sanitization.
   - Toggles the display of metadata and chunk content expansion.
   - Includes modals for viewing images and full metadata.
```

##### Auto generated documentation file from CodeViz.ai
