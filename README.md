# index.tsx

chat/src/index.tsx

```mermaid
graph TD;
    classDef mainNode fill:#f9f,stroke:#333,stroke-width:4px,color:black;
classDef otherNode fill:#ccf,stroke:#333,stroke-width:2px,color:black;
3153979318["<b>DatasetStart.tsx</b><br/><small>dashboard/src/pages/Dashboard/Dataset/</small>;"]:::mainNode;
subgraph "Inputs: Dashboard"
    823481955["<b>index.tsx</b><br/><small>dashboard/src/</small>;"]:::otherNode;
end;
823481955 --> 3153979318;
subgraph "Outputs: Dashboard;"
    1088935568["<b>apiTypes.ts</b><br/><small>dashboard/src/types/</small>;"]:::otherNode;
    1137686434["<b>UserContext.tsx</b><br/><small>dashboard/src/contexts/</small>;"]:::otherNode;
    2613122857["<b>DatasetContext.tsx</b><br/><small>dashboard/src/contexts/</small>;"]:::otherNode;
    730599621["<b>ApiKeyGenerateModal.tsx</b><br/><small>dashboard/src/components/</small>;"]:::otherNode;
    3300477352["<b>formatters.ts</b><br/><small>dashboard/src/</small>;"]:::otherNode;
end;
    3153979318 --> 1088935568;
    3153979318 --> 1137686434;
    3153979318 --> 2613122857;
    3153979318 --> 730599621;
    3153979318 --> 3300477352;
subgraph "Outputs: Server;"
    3745647460["<b>chunk_handler.rs</b><br/><small>server/src/handlers/</small>;"]:::otherNode;
    953673172["<b>user_handler.rs</b><br/><small>server/src/handlers/</small>;"]:::otherNode;
end;
    3153979318 --> 3745647460;
    3153979318 --> 953673172;
```

### Purpose
This file serves as the entry point for a Solid.js application. It initializes error tracking with Sentry in production environments and renders the main `Chat` component within a user context wrapper.

### Flow
1. **Imports**: The file imports necessary styles, libraries, and components.
2. **Sentry Initialization**: If the application is not in development mode (`!DEV`), Sentry is configured with a DSN and various integrations for error tracking and session replay.
3. **Rendering**: The `Chat` component is wrapped with `UserContextWrapper` and rendered into the DOM element with the id `root`.

##### Auto generated documentation file from CodeViz.ai