# monitor.py

monitoring_server/monitor.py

### Purpose
This file defines a FastAPI application with two endpoints, `/monitor_tracking` and `/monitor`, which are used to monitor tracking IDs by making POST requests to an external API. The endpoints check the status of the tracking IDs and return whether they are found or not.

### Flow
1. **Imports and Setup**:
   - Imports necessary modules and classes.
   - Defines a `TrackingRequest` model using Pydantic to validate incoming requests.

2. **FastAPI Application**:
   - Initializes a FastAPI app instance.

3. **/monitor_tracking Endpoint**:
   - Accepts a POST request with a JSON body containing a list of tracking IDs.
   - Requires `Authorization` and `TR-Dataset` headers.
   - Attempts to post the tracking IDs to an external API endpoint (`/api/chunks/tracking`) up to 300 times, with a 0.01-second delay between attempts.
   - Returns a status of "Found" if the external API responds with a 200 status code, otherwise returns "not found".

4. **/monitor Endpoint**:
   - Similar to `/monitor_tracking`, but posts to a different external API endpoint (`/api/chunks`).
   - Follows the same logic for retries and response handling.

##### Auto generated documentation file from CodeViz.ai
