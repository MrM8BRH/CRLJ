### Email Protocols:
Email communication relies on four key protocols:
1. **SMTP (Simple Mail Transfer Protocol):**
    - Responsible for sending and exchanging email messages between servers.
    - Operates at the application layer of the TCP/IP stack.
    - Used for transmitting email messages.
    - Ports: 25, 587
2. **POP3 (Post Office Protocol version 3):**
    - Retrieves email for a single client and allows offline access.
    - Requires emails to be downloaded from the server for access.
    - Limited to a single mailbox on the server.
    - Ports: 110
3. **IMAP (Internet Message Access Protocol):**
    - Retrieves email for multiple clients, supporting concurrent access.
    - Allows accessing and managing emails without downloading them.
    - Supports multiple mailboxes on different servers.
    - Enables email operations such as creating, manipulating, and deleting emails on the server.
    - Ports: 143
4. **MIME (Multipurpose Internet Mail Extensions):**
    - Extends email protocols to support non-ASCII data.
    - Enables sending and receiving various media types (e.g., audio, images, video) via email.
    - Allows sending multiple attachments in a single message and supports messages of unlimited length.
## Key Components of email flow:
- **Sender's Email Composition:**
    - The sender creates an email using **MUA** (Mail User Agent), such as an email client or web interface.
- **Sender Authentication and Structure Verification:**
    - The **MUA** sends the email to the **MSA** (Mail Submission Agent), which authenticates the sender and verifies the email's structure.
- **Email Routing through MTA:**
    - The **MSA** forwards the email to the **MTA** (Mail Transfer Agent).
    - The **MTA** determines the recipient's domain (e.g., abc.com) from the email address and performs a **DNS lookup** to retrieve the **MX record** (Mail Exchange record), which lists the mail servers for the recipient’s domain.
- **Email Routing to MX Server:**
    - The **MTA** efficiently routes the email to the appropriate **MX server** responsible for handling emails for the recipient's domain.
- **Delivery to Recipient's MDA:**
    - The **MX server** forwards the email to the **MDA** (Mail Delivery Agent), which stores the email in the recipient’s mailbox.
- **Recipient Access via MUA:**
    - The recipient accesses the email through their **MUA**, allowing them to view the message.
### Email Authentication Methods
To prevent email spoofing, domain owners define authentication records and rules to help receiving email servers determine whether to deliver an email to the recipient's inbox. There are three main email authentication protocols:
1. **SPF (Sender Policy Framework):**
    - Allows domain owners to specify which mail servers are authorized to send emails on behalf of their domain.
    - The domain owner creates an SPF record in DNS, listing the IP addresses of authorized mail servers.
    - When a receiving server gets an email, it compares the sender's IP address with those in the SPF record to decide whether to accept or reject the email.
2. **DKIM (DomainKeys Identified Mail):**
    - Ensures email content remains intact during transit and authenticates the sender.
    - The sender creates a digital signature by hashing and encrypting the email body and some header fields using a private key.
    - The public key is published in the domain’s DNS record. The receiving server uses this public key to verify the signature and confirm the email’s authenticity.
3. **DMARC (Domain-Based Message Authentication, Reporting, and Conformance):**
    - Works alongside SPF and DKIM to protect against email spoofing, phishing, and other fraud attempts.
    - Domain owners define a policy in DNS that specifies how to handle emails failing SPF or DKIM checks (e.g., reject, quarantine, or accept).
    - The receiving server follows the policy and sends a report to the domain owner detailing authentication results and potential misuse.
### Email Header    
An **email header** contains important metadata and information about an email’s journey from sender to recipient. While hidden by default for regular users, it is valuable for investigators, offering insights that help analyze the email, detect threats (such as spoofing), and track its origin. Key details include the sender, recipient, timestamps, IP addresses, and email authentication results.

> **Note**: The header is added in reverse order, meaning the top-most entry is the closest to the receiver.
#### Key Components of the Email Header:
- **From**: Sender's email address (can be spoofed or altered by the sender).
- **To**: Recipient's email address.
- **Subject**: The subject line of the email.
- **Date**: Timestamp when the email was sent.
- **Message-ID**: Unique identifier assigned by the sender’s mail server.
- **MIME-Version**: Indicates the format (e.g., text, HTML, attachments).
- **Content-Type**: Specifies the type of content in the email (e.g., plain text, HTML, multipart for attachments).
- **Received**:
    - Lists all the servers the email passed through, showing the path from sender to recipient.
    - Each **Received** line includes the server's IP address, domain, and timestamp.
    - The first **Received** line is the closest to the receiver.
    - Typical format: `Received: from [sender_server] by [receiving_server] with [protocol]; [timestamp]`
    - Example: `Received: from smtp.sender.com (192.0.2.1) by mail.recipient.com (198.51.100.1) with SMTP; Tue, 5 Jan 2025 10:23:45 -0500`
- **Reply-To**: The address where replies should be sent.
- **Return-Path**: Email address for bounce messages (e.g., undeliverable email notices).
- **Authentication Results**: Shows results of SPF, DKIM, and DMARC checks for email authentication.
#### **X-Headers (Non-Standard Headers)**
These headers are added by email servers, clients, or applications for additional information. They are typically prefixed with "X-" to differentiate them from standard headers and may vary in purpose depending on the system:
- **X-Originating-IP**: Displays the IP address of the original sender.
    - Example: `X-Originating-IP: [192.0.2.1]`
    - Useful for tracing the origin of an email, especially in cases of spam or phishing.
- **X-Mailer**: Indicates the email client or application used to send the email.
    - Example: `X-Mailer: Microsoft Outlook 16.0`
    - Useful for identifying the sender’s email software.
- **X-Spam-Status**: Shows whether the email was flagged as spam by the receiving server’s filter.
    - Example: `X-Spam-Status: Yes`
    - Helps understand why an email was flagged as spam.
- **X-Spam-Score**: Provides a score based on spam-detection algorithms.
    - Example: `X-Spam-Score: 5.6`
    - The higher the score, the more likely the email is spam.
