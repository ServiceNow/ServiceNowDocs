---
title: Redact sensitive data from documents
description: Manually mask sensitive content or data from your PDF documents. Data redaction is available in configurable workspaces.
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Redact sensitive data from documents

Manually mask sensitive content or data from your PDF documents. Data redaction is available in configurable workspaces.

## Data redaction

Only documents in the Published or Draft state are eligible for data redaction.

Sensitive data can be redacted by searching for a keyword or by selecting and drawing over any area in PDF that needs to be masked. The search and redact option is applicable only for text and not for images.

**Note:**

-   Paragraphs or keywords split into multiple consecutive lines can't be redacted together while using the search and redact option for a keyword or phrase.
-   In some instances search and redact might not hide special characters that are prefixed or suffixed with the text, such as "manual:" or ".PDF".
-   In some cases during manual redaction, the text or redaction marks may overlap other sections of the PDF. This overlap can cause the original text to be removed and replaced with white space.
-   Data redaction is not possible if the PDF includes non-parseable images, like those in JBIG2 format.

-   **[Redact data from documents](../task/redact-sensitive-data.md)**  
Redact sensitive data from PDF documents by either searching keywords or selecting text.

**Parent Topic:**[Using Document Management](using-document-management.md)

