# ContextWrapper.tsx

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
2335540861["<b>ContextWrapper.tsx</b><br/><small>dashboard/src/layouts/</small>"]:::mainNode

```
### Purpose
The `ContextWrapper` component is designed to provide context to its child components. It wraps its children with `UserContextWrapper` and `DatasetContextWrapper`, ensuring that user and dataset context are available throughout the component tree.

### Flow
1. **Import Statements**: The file imports necessary modules from "solid-js" and context wrappers from the `contexts` directory.
2. **Interface Definition**: Defines `ContextWrapperProps` to type the `children` prop.
3. **ContextWrapper Component**: 
   - Wraps its children with `UserContextWrapper`.
   - Inside `UserContextWrapper`, it further wraps the children with `DatasetContextWrapper`.
   - This nested structure ensures that both user and dataset contexts are provided to the children components.

##### Auto generated documentation file from CodeViz.ai
