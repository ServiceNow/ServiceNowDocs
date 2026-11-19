---
title: Document Intelligence processing with playbook
description: Invoices ingested through Document Intelligence require Accounts Payable specialists or admins to perform manual actions depending on Document Intelligence availability and invoice processing using Document Intelligence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/use-di-with-playbook.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Playbook for updating the invoice primary data, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Document Intelligence processing with playbook

Invoices ingested through Document Intelligence require Accounts Payable specialists or admins to perform manual actions depending on Document Intelligence availability and invoice processing using Document Intelligence.

The following scenarios occur when Document Intelligence process a document:

-   When Document Intelligence is processing the document, and if you select the **Capture invoice details** card, you’re prompted with the message: `Invoice is currently being processed by DocIntel. This process might take some time to complete. Check back for updates.`
-   When Document Intelligence processing is completed and the data is extracted successfully, the **Capture invoice details** card is auto-completed and displays the message as: `Invoice extraction is successfully completed`.
-   [Extract data with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/extract-data-with-di.md)
-   [Extract data when Document Intelligence fails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/extract-data-when-di-fails.md)
-   [Extract data when Document Intelligence is unavailable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/extract-data-when-di-is-unavailable.md)

-   **[Extract data with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/extract-data-with-di.md)**  
You can manually extract data from the document when Document Intelligence completes the processing but fails to auto-extract data.
-   **[Extract data when Document Intelligence fails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/extract-data-when-di-fails.md)**  
You must manually create an invoice for processing when Document Intelligence fails to process the task.
-   **[Extract data when Document Intelligence is unavailable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/extract-data-when-di-is-unavailable.md)**  
You must manually create an invoice for processing when Document Intelligence is unavailable.

**Parent Topic:**[Playbook for updating the invoice primary data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/playbooks.md)

