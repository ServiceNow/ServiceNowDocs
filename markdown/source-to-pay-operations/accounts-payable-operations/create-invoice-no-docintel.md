---
title: Create an invoice manually when Document Intelligence is unavailable
description: As an Account Payable Specialist, manually create an invoice if an invoice processing case automatically is created when the Document Intelligence application is unavailable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice-no-docintel.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Invoice ingestion process when Document Intelligence is unavailable, Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create an invoice manually when Document Intelligence is unavailable

As an Account Payable Specialist, manually create an invoice if an invoice processing case automatically is created when the Document Intelligence application is unavailable.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Do one of the following:

    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice processing cases**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice processing cases**.
4.  Open the invoice processing case.

5.  Select **Create invoice**.

    The invoice is created and the invoice processing case displays the following message:

    `Invoice has been successfully created. Verify all the required fields are correct and add invoice lines before submitting.`

    Verify that the values in the invoice fields are correct and ensure that you add at least one invoice line for the invoice. For more information, see [Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md).

6.  Select **Submit invoice**.


## Result

The invoice is manually created when the Document Intelligence application is unavailable.

**Parent Topic:**[Invoice ingestion process when Document Intelligence is unavailable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/invoice-ingest-docintel-unavailable.md)

