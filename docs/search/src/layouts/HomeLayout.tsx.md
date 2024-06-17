# HomeLayout.tsx

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
2947139446["<b>HomeLayout.tsx</b><br/><small>search/src/layouts/</small>"]:::mainNode

```
### Purpose
The `Home` component serves as the main entry point for the home page of the application. It sets the theme based on user preferences, registers a service worker for offline capabilities, and wraps the main content with necessary context providers.

### Flow
1. **Theme Initialization**: The component determines the theme (`light` or `dark`) based on local storage or the user's system preferences. It then applies the appropriate class to the document's root element.
2. **Service Worker Registration**: If supported, the component registers a service worker when the window loads to enable offline functionality.
3. **Rendering**: The component returns a JSX structure that includes:
   - `DatasetAndUserContextWrapper`: Provides context for dataset and user information.
   - `HomeSearch`: A component likely responsible for the search functionality on the home page.
   - `ShowToast`: A component for displaying toast notifications.

##### Auto generated documentation file from CodeViz.ai
