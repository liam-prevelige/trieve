# email_operator.rs

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
3600531853["<b>email_operator.rs</b><br/><small>server/src/operators/</small>"]:::mainNode

```
### Purpose
This file is responsible for sending emails using SMTP. It retrieves SMTP credentials from environment variables and constructs and sends an email with a specified HTML body to a given recipient.

### Flow
1. **Retrieve SMTP Credentials**: The `get_smtp_creds` function fetches the SMTP username and password from environment variables using the `get_env!` macro. It returns these credentials wrapped in a `Credentials` object.

2. **Send Email**: The `send_email` function:
   - Retrieves the SMTP relay and email address from environment variables.
   - Calls `get_smtp_creds` to get the SMTP credentials.
   - Constructs an `SmtpTransport` object using the relay and credentials.
   - Builds an email message with the provided HTML body and recipient address.
   - Sends the email using the `mailer.send` method and handles any errors that occur during the sending process.

##### Auto generated documentation file from CodeViz.ai
