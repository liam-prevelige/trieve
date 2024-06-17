# invitation_handler.rs

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
1350479552["<b>invitation_handler.rs</b><br/><small>server/src/handlers/</small>"]:::mainNode

```
### Purpose
This file handles the invitation system for an organization. It includes functionalities to create, send, retrieve, and delete invitations. The invitations allow users to join an organization with a specified role.

### Flow
1. **Email Validation**: The `email_regex` function provides a regex pattern to validate email addresses.
2. **Data Structures**: 
   - `InvitationResponse`: Structure for the response containing the registration URL.
   - `InvitationData`: Structure for the request payload containing details like organization ID, user role, email, app URL, and redirect URI.
3. **Endpoints**:
   - **POST /invitation**: 
     - Validates the email format.
     - Checks if the user has the appropriate role to invite another user.
     - Adds an existing user to the organization or creates a new invitation.
     - Sends the invitation email.
   - **GET /invitation/{organization_id}**: Retrieves all invitations for a specified organization.
   - **DELETE /invitation/{invitation_id}**: Deletes an invitation by its ID.
4. **Helper Functions**:
   - `create_invitation`: Creates an invitation and generates a registration URL.

##### Auto generated documentation file from CodeViz.ai
