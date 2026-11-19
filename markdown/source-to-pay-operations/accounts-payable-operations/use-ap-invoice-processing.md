---
title: Using Accounts Payable Invoice Processing
description: Accounts Payable Specialists can use the Accounts Payable Invoice Processing application to manage and work on invoice processing cases to perform end-to-end invoice processing, from invoice ingestion to approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Using Accounts Payable Invoice Processing

Accounts Payable Specialists can use the Accounts Payable Invoice Processing application to manage and work on invoice processing cases to perform end-to-end invoice processing, from invoice ingestion to approval.

-   **[Invoice ingestion using the AP Invoice API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/invoice-ingestion-using-api.md)**  
The AP Invoice API enables bulk import of AP invoices from external systems, such as supplier billing platforms and OCR solutions, into Accounts Payable Operations using cXML, JSON, or XML.
-   **[Rules based engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/rules-based-engine.md)**  
The rule based engine maps the invoice line with purchase order line using fields such as unit price, delivered unit price, exact description, exact amount and amount round off.
-   **[Work with invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-invoices.md)**  
Invoices are generated for a payment against a purchase order. The Accounts Payable Specialist \[sn\_ap\_apm.accounts\_payable\_specialist\] can access all the invoices and take required actions to process the invoices in Source-to-Pay Workspace.
-   **[Invoice processing cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/working-with-ingestion-cases.md)**  
Typically, Accounts Payable Operations integration with Document Intelligence automatically creates the invoice processing case by extracting data from the invoice that you receive as an attachment via email. However, the Accounts Payable Specialist may need to manually create a new invoice or update details of a partially created invoice in situations where the automated invoice creation process encounters issues or is not available.
-   **[Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md)**  
Invoice exceptions are discrepancies identified during invoice processing that must be resolved before payment, such as missing information, tax variances, or supplier issues.
-   **[Tolerance Rules and Variances for invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tolerance-rules-and-variance.md)**  
Tolerance rules define the limits set on an invoice to determine the permissible amount of variance that can be applied to an invoice before the invoice total exceeds the tolerance limit.
-   **[Invoice approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/invoice-approvals.md)**  
Invoices with the No exceptions found status are eligible for approval.
-   **[View invoice documents in the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/view-invoice-attachment.md)**  
View the invoice documents directly in the Source-to-Pay Workspace using Document Viewer without having to download them.

**Parent Topic:**[Use Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article about invoice]()

[Invoice case categories and subcategories]()

[Using Invoice Case Management]()

[Advanced Work Assignment in Accounts Payable Operations]()

[Configure Advanced Work Assignment for Accounts Payable Operations]()

[Using Advanced Work Assignment for Accounts Payable Operations]()

[Working with Advanced Work Assignment]()

[Interaction management in Accounts Payable Operations]()

[Composing emails with predefined content from the Source-to-Pay Workspace]()

[Universal Request in Accounts Payable Operations]()

[Playbook for updating the invoice primary data]()

[Using Supplier Collaboration Portal in APO]()

