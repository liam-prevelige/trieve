# redoc_ci.rs

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
2170716456["<b>redoc_ci.rs</b><br/><small>server/src/bin/</small>"]:::mainNode

```
### Purpose
This file generates and prints a pretty-formatted JSON representation of the OpenAPI documentation for the `trieve_server` API.

### Flow
1. **Imports**: The file imports `ApiDoc` from `trieve_server` and `OpenApi` from `utoipa`.
2. **Main Function**: 
   - Calls `ApiDoc::openapi()` to generate the OpenAPI documentation.
   - Converts the documentation to a pretty-formatted JSON string using `to_pretty_json()`.
   - Prints the JSON string to the console.
   - Returns `Ok(())` to indicate successful execution.

##### Auto generated documentation file from CodeViz.ai
