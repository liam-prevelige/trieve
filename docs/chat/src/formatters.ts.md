# formatters.ts

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
726797618["<b>formatters.ts</b><br/><small>chat/src/</small>"]:::mainNode

```
### Purpose
This file provides utility functions and constants for formatting numbers and byte sizes. It includes a formatter for USD currency, a function to format byte sizes into human-readable strings, and a general number formatter.

### Flow
1. **USD Formatter**: 
   ```javascript
   export const usdFormatter = new Intl.NumberFormat("en-US", {
     style: "currency",
     currency: "USD",
   });
   ```
   - Creates a formatter for USD currency using the `Intl.NumberFormat` API.

2. **Byte Size Formatter**:
   ```javascript
   export function formatBytesDecimal(bytes: number, dm = 2) {
     if (bytes == 0) return "0 Bytes";
     if (bytes > 1e8) {
       return (bytes / 1e9).toFixed(dm) + " GB";
     }
     return (bytes / 1e6).toFixed(dm) + " MB";
   }
   ```
   - Converts byte sizes into a human-readable format (GB or MB) with a specified number of decimal places.

3. **Number Formatter**:
   ```javascript
   export const numberFormatter = new Intl.NumberFormat("en-US");
   ```
   - Creates a general number formatter for the "en-US" locale.

##### Auto generated documentation file from CodeViz.ai
