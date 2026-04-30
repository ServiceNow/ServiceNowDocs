---
title: PDF generation and accessibility
description: PDF generation settings support accessibility features such as accessibility tags for screen readers, customizable export formats, and image retrieval timeouts for optimized HTML to PDF conversion.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# PDF generation and accessibility

PDF generation settings support accessibility features such as accessibility tags for screen readers, customizable export formats, and image retrieval timeouts for optimized HTML to PDF conversion.

**Note:** PDF generation with accessibility is unavailable for on-premise customers.

## Accessible PDF

To enable accessibility for PDF generation, add the accessibility property **com.snc.pdf.generation.accessibility** and set the value to `true`. Only users with admin roles can set the property. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

For PDF generation API, see [PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

## Image retrieval timeout in HTML to PDF conversation

To specific the time out duration for HTML to PDF conversion update the timeout value for the system property **com.snc.pdf.html2pdf.image\_retrieval\_timeout**. This property enables you to specify an image retrieval timeout in seconds.

-   **[Export to PDF](export-to-pdf.md)**  
Export an individual record or list of records into a PDF format that supports accessibility. When this feature is enabled, accessibility tags are available in the PDF tag tree to help users who rely on-screen readers to navigate, understand, and interact with the generated PDF documents.
-   **[Guardrails for PDF generation and accessibility](guardrails-pdf-generation-accessibility.md)**  
Static and dynamic guardrails are safeguards that help maintain stability during PDF generation. Static guardrails enforce fixed limits like maximum PDF size, while dynamic guardrails monitor real-time memory usage and terminate exports when memory pressure exceeds a defined threshold.

**Parent Topic:**[Document Services](../reference/document-services-landing-page.md)

