# OrgFiles.tsx

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
3517505518["<b>OrgFiles.tsx</b><br/><small>search/src/pages/file/</small>"]:::mainNode

```
### Purpose
The `OrgFiles` component is designed to provide a user interface for viewing and managing organizational files. It integrates various sub-components to offer functionalities such as file viewing, deletion confirmation, and layout structuring.

### Flow
1. **State Management**: 
   - `showConfirmGroupDeleteModal` and `onGroupDelete` signals are created to manage the visibility of the confirmation modal and the delete action respectively.

2. **Layout**:
   - The component is wrapped in a `SearchLayout` to provide a consistent layout structure.
   - Inside the layout, a `div` container is used to hold the main content with specific styling for margins, padding, and text size.

3. **File Viewing and Deletion**:
   - `OrgFileViewPage` is rendered to display the organizational files. It receives `setOnDelete` and `setShowConfirmModal` as props to handle file deletion.
   - `ConfirmModal` is rendered to show a confirmation dialog when a delete action is triggered. It uses the `showConfirmGroupDeleteModal` signal to control its visibility and `onGroupDelete` to execute the delete action.

4. **Footer**:
   - A `Footer` component is included at the bottom of the layout for additional navigation or information.

The component ensures that users can view files and confirm deletions through a modal, maintaining a clean and organized layout.

##### Auto generated documentation file from CodeViz.ai
