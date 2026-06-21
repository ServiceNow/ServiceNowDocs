---
title: Create invoice cost allocation manually
description: Manually allocate invoice line cost across multiple cost centers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/source-to-pay-operations/accounts-payable-operations/create-invoice-cost-allocation.html
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-09-25"
reading_time_minutes: 1
breadcrumb: [Invoice cost allocation, Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Create invoice cost allocation manually

Manually allocate invoice line cost across multiple cost centers.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist, admin

## Procedure

1.  Navigate to **All** &gt; **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Navigate to **Lists** &gt; **Invoices** &gt; **All Open Invoices**.

3.  Select an **invoice** &gt; **Invoice line**.

    For more information on invoice line, see [Create an invoice manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/source-to-pay-operations/accounts-payable-operations/create-invoice.md).

4.  Select **Cost allocations**.

5.  Select **New**.

    The invoice cost allocation form displays. For more information on the cost allocation form, see [Create invoice cost allocation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/source-to-pay-operations/accounts-payable-operations/create-invoice-cost-allocation-form.md)

    **Note:**

    -   During cost allocation, if the total allocated quantity or amount across different cost centers or ledger accounts isn’t equal to the invoice line quantity or subtotal, then the invoice cost allocation exception occurs. For more information on exceptions, see [Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md).
    -   When you delete an invoice line record, you’re prompted with a pop-up message to confirm the deletion of an invoice line record removes its associated cost allocation record.
6.  Select **Save**.


## Result

The cost allocation form is added to the invoice line.

**Parent Topic:**[Invoice cost allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/source-to-pay-operations/accounts-payable-operations/invoice-line-cost-allocation.md)

