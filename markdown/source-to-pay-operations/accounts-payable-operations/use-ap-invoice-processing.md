---
title: Using Accounts Payable Invoice Processing
description: Accounts Payable Specialists can use the Accounts Payable Invoice Processing application to manage and work on invoice processing cases to perform end-to-end invoice processing, from invoice ingestion to approval.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Using Accounts Payable Invoice Processing

Accounts Payable Specialists can use the Accounts Payable Invoice Processing application to manage and work on invoice processing cases to perform end-to-end invoice processing, from invoice ingestion to approval.

-   **[Invoice ingestion using Application programming interface \(API\)](invoice-ingestion-using-api.md)**  
The invoice ingestion API enables customers to ingest bulk AP invoices from external systems such as supplier billing systems, buyer network, and OCR solutions, supplier networks into APO. The supported payload formats are cXML, JSON and XML.
-   **[Rules based engine](rules-based-engine.md)**  
The rule based engine maps the invoice line with purchase order line using fields such as unit price, delivered unit price, exact description, exact amount and amount round off.
-   **[Work with invoices](work-with-invoices.md)**  
Invoices are generated for a payment against a purchase order. The Accounts Payable Specialist \[sn\_ap\_apm.accounts\_payable\_specialist\] can access all the invoices and take required actions to process the invoices in Source-to-Pay Workspace.
-   **[Invoice processing cases](working-with-ingestion-cases.md)**  
Typically, Accounts Payable Operations integration with Document Intelligence automatically creates the invoice processing case by extracting data from the invoice that you receive as an attachment via email. However, the Accounts Payable Specialist may need to manually create a new invoice or update details of a partially created invoice in situations where the automated invoice creation process encounters issues or is not available.
-   **[Invoice exceptions](work-with-invoice-exceptions.md)**  
Invoice exceptions are issues that are identified in an invoice during invoice processing.
-   **[Tolerance Rules and Variances for invoices](tolerance-rules-and-variance.md)**  
Tolerance rules define the limits set on an invoice to determine the permissible amount of variance that can be applied to an invoice before the invoice total exceeds the tolerance limit.
-   **[Invoice approvals](invoice-approvals.md)**  
Invoices with the No exceptions found status are eligible for approval.
-   **[View invoice documents in the Source-to-Pay Workspace](../task/view-invoice-attachment.md)**  
View the invoice documents directly in the Source-to-Pay Workspace using Document Viewer without having to download them.

**Parent Topic:**[Using Accounts Payable Operations](use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article about invoice](../task/create-knowledge-base-articles-for-invoices.md)

[Invoice case categories and subcategories](working-with-cases.md)

[Using Invoice Case Management](use-invoice-case-mgmt.md)

[Advanced Work Assignment in Accounts Payable Operations](advanced-work-assignment.md)

[Configure Advanced Work Assignment for Accounts Payable Operations](../task/configure-advanced-work-assignment-for-apo.md)

[Using Advanced Work Assignment for Accounts Payable Operations](using-awa-for-apo.md)

[Working with Advanced Work Assignment](../task/working-with-advanved-work-assignment.md)

[Interaction management in Accounts Payable Operations](interaction-record.md)

[Composing emails with predefined content from the Source-to-Pay Workspace](email-composer-apm-workspace.md)

[Universal Request in Accounts Payable Operations](universal-request-in-apo.md)

[Playbook for updating the invoice primary data](playbooks.md)

[Using Supplier Collaboration Portal in APO](using-supplier-collaboration-portal.md)

