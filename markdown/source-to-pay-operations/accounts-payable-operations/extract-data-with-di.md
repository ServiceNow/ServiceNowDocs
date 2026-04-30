---
title: Extract data with Document Intelligence
description: You can manually extract data from the document when Document Intelligence completes the processing but fails to auto-extract data.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document Intelligence processing with playbook, Playbook for updating the invoice primary data, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Extract data with Document Intelligence

You can manually extract data from the document when Document Intelligence completes the processing but fails to auto-extract data.

## Before you begin

Role required: Accounts Payable admin, Accounts Payable specialist

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

    A list of options within the workspace is displayed.

3.  Select **Invoices &gt;****All invoices.**

    You can create an invoice manually. For more information on invoices, see [Work with invoices](../concept/work-with-invoices.md).

4.  Select **View invoice processing case**.

    A playbook is created for the invoice processing case.

5.  Select **Validate invoice** &gt;**Capture invoice details** activity card.

    An alert message displays as: `Review the invoice details captured by DocIntel and provide any missing information`.

6.  Select **Review invoice**.

    The document extraction dashboard opens in a tab. The document extraction dashboard extracts the invoice fields.

    **Note:**

    -   When the document extraction is completed either automatically or manually and all the required invoice details are populated, then the invoice is submitted automatically. The **Review header details** and **Review invoice lines** cards are set to auto-complete.
    -   When the document extraction is completed either automatically or manually, but the required fields are missing, then manually populate the invoice line fields or add invoice lines using **Review invoice lines**.
    For more information on manual creation of invoice, see [Using Invoice Case Management](../concept/use-invoice-case-mgmt.md).

7.  Select **Submit**.


## Result

The data is manually extracted from the document.

**Parent Topic:**[Document Intelligence processing with playbook](../concept/use-di-with-playbook.md)

