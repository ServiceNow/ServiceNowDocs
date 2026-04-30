---
title: Create invoice cost allocation manually
description: Manually allocate invoice line cost across multiple cost centers.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Invoice cost allocation, Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create invoice cost allocation manually

Manually allocate invoice line cost across multiple cost centers.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist, admin

## Procedure

1.  Navigate to **All** &gt; **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Navigate to **Lists** &gt; **Invoices** &gt; **All Open Invoices**.

3.  Select an **invoice** &gt; **Invoice line** &gt; .

    For more information on invoice line, see [Create an invoice manually](create-invoice.md).![Select the invoice line](../image/apo-create-cost-allocation.png)

4.  Select **Cost allocations**.

    ![Create a cost allocation](../image/apo-cost-allocate-tab.png)

5.  Select **New**.

    The invoice cost allocation form displays. For more information on the cost allocation form, see [Create invoice cost allocation form](../reference/create-invoice-cost-allocation-form.md)

    **Note:**

    -   During cost allocation, if the total allocated quantity or amount across different cost centers or ledger accounts isn’t equal to the invoice line quantity or subtotal, then the invoice cost allocation exception occurs. For more information on exceptions, see [Invoice exceptions](../concept/work-with-invoice-exceptions.md).
    -   When you delete an invoice line record, you’re prompted with a pop-up message to confirm the deletion of an invoice line record removes its associated cost allocation record.
    -   When you select allocation type as cost center for the first record and save the changes, the subsequent records also will inherit the same allocation type.
6.  Select **Save**.


## Result

The cost allocation form is added to the invoice line.

**Parent Topic:**[Invoice cost allocation](../concept/invoice-line-cost-allocation.md)

**Related topics**  


[Accounts Payable Invoice Processing](../concept/acc-pay-invoice-processing.md)

[Invoice Case Management](../concept/acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](../concept/acc-pay-workspace.md)

[Using Now Assist for Accounts Payable Operations \(APO\)](../concept/using-now-assist-apo.md)

[Invoice processing cases](../concept/working-with-ingestion-cases.md)

[Invoice exceptions](../concept/work-with-invoice-exceptions.md)

