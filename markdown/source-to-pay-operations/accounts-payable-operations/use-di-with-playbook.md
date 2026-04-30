---
title: Document Intelligence processing with playbook
description: Invoices ingested through Document Intelligence require Accounts Payable specialists or admins to perform manual actions depending on Document Intelligence availability and invoice processing using Document Intelligence.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook for updating the invoice primary data, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Document Intelligence processing with playbook

Invoices ingested through Document Intelligence require Accounts Payable specialists or admins to perform manual actions depending on Document Intelligence availability and invoice processing using Document Intelligence.

The following scenarios occur when Document Intelligence process a document:

-   When Document Intelligence is processing the document, and if you select the **Capture invoice details** card, you’re prompted with the message: `Invoice is currently being processed by DocIntel. This process might take some time to complete. Check back for updates.`
-   When Document Intelligence processing is completed and the data is extracted successfully, the **Capture invoice details** card is auto-completed and displays the message as: `Invoice extraction is successfully completed`.
-   [Extract data with Document Intelligence](../task/extract-data-with-di.md)
-   [Extract data when Document Intelligence fails](../task/extract-data-when-di-fails.md)
-   [Extract data when Document Intelligence is unavailable](../task/extract-data-when-di-is-unavailable.md)

-   **[Extract data with Document Intelligence](../task/extract-data-with-di.md)**  
You can manually extract data from the document when Document Intelligence completes the processing but fails to auto-extract data.
-   **[Extract data when Document Intelligence fails](../task/extract-data-when-di-fails.md)**  
You must manually create an invoice for processing when Document Intelligence fails to process the task.
-   **[Extract data when Document Intelligence is unavailable](../task/extract-data-when-di-is-unavailable.md)**  
You must manually create an invoice for processing when Document Intelligence is unavailable.

**Parent Topic:**[Playbook for updating the invoice primary data](playbooks.md)

