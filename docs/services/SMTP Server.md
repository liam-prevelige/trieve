# SMTP Server Service

```mermaid
graph TD;
    classDef mainNode fill:#a8dadc,stroke:#333,stroke-width:4px;
classDef otherNode fill:#f1faee,stroke:#333,stroke-width:2px;
2["<b>SMTP Server</b><br/><small>services</small>"]:::mainNode

```

## Usage Details
- **/server/src/operators/email_operator.rs** - This file contains the core functionality for sending emails using the SMTP server. The `get_smtp_creds` function retrieves the SMTP username and password from environment variables, encapsulating them in a `Credentials` object. The `send_email` function is responsible for constructing and sending the email. It retrieves the SMTP relay and email address from environment variables, builds the email message with the provided HTML body and recipient address, and sends it using the `SmtpTransport` object. Error handling is implemented to log any issues that occur during the email sending process and return a `ServiceError` if necessary.

## Additional Notes
- **Environment Variables**: The service relies heavily on environment variables (`SMTP_USERNAME`, `SMTP_PASSWORD`, `SMTP_RELAY`, and `SMTP_EMAIL_ADDRESS`) for configuration. Ensure these variables are correctly set in the environment where the application is running.
- **Error Handling**: Proper error handling is in place to log errors and return a user-friendly message if the email fails to send. This is crucial for debugging and maintaining the reliability of the email service.
- **Security**: Storing SMTP credentials in environment variables helps in keeping sensitive information secure and separate from the codebase. Ensure that these environment variables are managed securely, especially in production environments.