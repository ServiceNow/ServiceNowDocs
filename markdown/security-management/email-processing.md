---
title: Security Operations email processing
description: You can set up the integration of information from external detection systems, provide granularity in processing security operations records, handle unmatched emails, and prevent duplication of records using Email Processing.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Operations common functionality, Security Operations]
---

# Security Operations email processing

You can set up the integration of information from external detection systems, provide granularity in processing security operations records, handle unmatched emails, and prevent duplication of records using Email Processing.

Email Processing consists of these features:

|Feature|Description|
|-------|-----------|
|Email Parsing|Generate new Security Operations records from external system emails.|
|Duplication Rules|Identifies new email with known incidents and processes them appropriately.|
|Properties|Specifies accounts used as input in Email Parsing for security, vulnerability, and IoCs. Provides for granularity in processing Security Operations records.|
|Unmatched Emails|Lists emails that do not match any Security Operations record.|

-   **[Security Operations email properties](email-properties.md)**  
Email Properties specify which inboxes are used as input in Email Parsing to import information from external detection systems to create records for security, vulnerability, and IoCs. You can set up a general account for all external detection systems to use, or individual email accounts for Security Incident Response, Threat Intelligence, or Vulnerability Response.
-   **[Security Operations email parsing](email-parsing.md)**  
Generate new Security Operations records from external detection systems using Email Parsing. This feature provides a method for integrating information from external tools such as malware detection, vulnerability detection, firewalls, threat intelligence, and more.
-   **[Unmatched Security Operations email events](umatched-emails.md)**  
Email events that do not match an email parser have their "matched" flag unset. You can view these email event records from the Unmatched Emails list, to reveal external detection systems whose emails are not yet parsed.

**Parent Topic:**[Security Operations common functionality](sec-ops-common-functionality.md)

