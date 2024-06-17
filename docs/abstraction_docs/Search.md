# Search

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
16["<b>Search</b><br/><small>abstraction_docs</small>"]:::mainNode

```

## Core Functionality
- **Search Interface**: `SearchForm.tsx` provides the main search form, allowing users to input queries, select search types, and apply filters.
- **User and Dataset Management**: `DatasetAndUserContext.tsx` manages user authentication, organization selection, and dataset information.
- **Filtering**: `FilterModal.tsx` allows users to apply and manage filters for search results.
- **Type Definitions and Utilities**: `apiTypes.ts` defines TypeScript interfaces and utility functions for handling metadata and user data.
- **Notifications**: `ShowToasts.tsx` implements a toast notification system for success and error messages.
- **Dropdowns and Modals**: `ComboboxChecklist.tsx`, `ConfirmModal.tsx`, and `FullScreenModal.tsx` provide UI components for dropdowns and modal dialogs.
- **Metadata Display**: `ChunkMetadataDisplay.tsx` displays metadata and content for specific data chunks.
- **Bookmark Management**: `BookmarkPopover.tsx` manages bookmarks and groups for data chunks.
- **Chunk Management**: `ScoreChunk.tsx` and `ScoreChunkArray.tsx` display and manage chunks of data, including navigation and metadata.
- **Tooltips and Input Forms**: `Tooltip.tsx` and `InputRowsForm.tsx` provide UI components for tooltips and input forms.
- **Image Display**: `ImageModal.tsx` displays images in a modal dialog.
- **Home Page Layout**: `HomeLayout.tsx` and `HomeSearch.tsx` set up the main layout and search interface for the home page.
- **Navigation**: `HomeNavbar.tsx` and `Navbar.tsx` provide navigation bars for the application.
- **Suggested Queries**: `DefaultQueries.tsx` and `SuggestedQueries.tsx` display suggested search queries.
- **Footer**: `Footer.tsx` provides a consistent footer section with social media links and theme control.
- **Organization and Dataset Selection**: `OrganizationSelectBox.tsx` and `DatasetSelectBox.tsx` provide dropdowns for selecting organizations and datasets.
- **Theme Control**: `ThemeModeController.tsx` allows users to toggle between light, dark, and system theme modes.
- **Group and File Management**: `OrgGroups.tsx`, `OrgFiles.tsx`, `OrgGroupPageView.tsx`, and `OrgFilePageView.tsx` manage organizational groups and files.
- **Search Results**: `ResultsPage.tsx` displays search results with pagination and filtering options.
- **Document Chunk Management**: `CreateChunk.tsx`, `EditChunk.tsx`, `ViewChunk.tsx`, `CreateNewDocChunkForm.tsx`, and `EditChunkPageForm.tsx` provide interfaces for creating, editing, and viewing document chunks.
- **404 Page**: `404.tsx` displays a 404 error page for non-existent routes.
- **Service Worker**: `sw.js` sets up a service worker for offline capabilities.
- **Date Picker**: `DatePicker.tsx` provides a UI component for selecting date ranges.
- **Chat Interface**: `ChatPopup.tsx` and `AfMessage.tsx` implement a chat interface for user interactions with search results.
- **Routing and Initialization**: `index.tsx` sets up routing and initializes the application.