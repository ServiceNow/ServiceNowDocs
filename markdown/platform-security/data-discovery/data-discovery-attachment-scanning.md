---
title: Attachment scanning in Data Discovery jobs
description: Attachment scanning in Data Discovery enables you to scan, discover, and report on sensitive data in file attachments.
locale: en-US
release: yokohama
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2025-03-24"
reading_time_minutes: 1
breadcrumb: [Configure a Data Discovery job, Data Discovery jobs, Data Discovery, Platform Privacy]
---

# Attachment scanning in Data Discovery jobs

Attachment scanning in Data Discovery enables you to scan, discover, and report on sensitive data in file attachments.

Sensitive data such as social security Numbers \(SSN\), credit card numbers, and other personally identifiable information \(PII\) are often contained in file attachments. Data Discovery jobs attachment scanning, enables you to discover and report sensitive data in certain attachments.The attachment scanning feature is only available for scheduled scans.

**Warning:** This feature requires sending your data to a controlled ServiceNow environment. Contact your account and support teams for enabling the attachment scanning feature

## Limitations

-   Embedded images and attachments in PDF and DOC files will not be scanned for sensitive data.
-   Files must be less than 10MB.
-   Support is available for the following file types:
    -   PDF
    -   DOC\(X\)
    -   TXT

