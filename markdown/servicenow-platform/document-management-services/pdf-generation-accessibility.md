---
title: PDF generation and accessibility
description: PDF generation settings support accessibility features such as accessibility tags for screen readers, customizable export formats, and image retrieval timeouts for optimized HTML to PDF conversion.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# PDF generation and accessibility

PDF generation settings support accessibility features such as accessibility tags for screen readers, customizable export formats, and image retrieval timeouts for optimized HTML to PDF conversion.

**Note:** PDF generation with accessibility is unavailable for on-premise customers.

## Accessible PDF

To enable accessibility for PDF generation, add the accessibility property **com.snc.pdf.generation.accessibility** and set the value to `true`. Only users with admin roles can set the property. For more information, see Add a system property.

For PDF generation API, see PDFGenerationAPI - Scoped, Global

## Image retrieval timeout in HTML to PDF conversation

To specific the time out duration for HTML to PDF conversion update the timeout value for the system property **com.snc.pdf.html2pdf.image\_retrieval\_timeout**. This property enables you to specify an image retrieval timeout in seconds.

-   **[Export to PDF](export-to-pdf.md)**  
Export an individual record or list of records into a PDF format that supports accessibility. When this feature is enabled, accessibility tags are available in the PDF tag tree to help users who rely on-screen readers to navigate, understand, and interact with the generated PDF documents.
-   **[Guardrails for PDF generation and accessibility](guardrails-pdf-generation-accessibility.md)**  
Static and dynamic guardrails are safeguards that help maintain stability during PDF generation. Static guardrails enforce fixed limits like maximum PDF size, while dynamic guardrails monitor real-time memory usage and terminate exports when memory pressure exceeds a defined threshold.

**Parent Topic:**[Document Services](../reference/document-services-landing-page.md)

