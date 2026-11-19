---
title: Create invoice cost allocation manually
description: Manually allocate invoice line cost across multiple cost centers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice-cost-allocation.html
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

    For more information on invoice line, see [Create an invoice manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice.md).\[Omitted image "apo-create-cost-allocation.png"\] Alt text: Select the invoice line

4.  Select **Cost allocations**.

    \[Omitted image "apo-cost-allocate-tab.png"\] Alt text: Create a cost allocation

5.  Select **New**.

    The invoice cost allocation form displays. For more information on the cost allocation form, see [Create invoice cost allocation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-invoice-cost-allocation-form.md)

    **Note:**

    -   During cost allocation, if the total allocated quantity or amount across different cost centers or ledger accounts isn’t equal to the invoice line quantity or subtotal, then the invoice cost allocation exception occurs. For more information on exceptions, see [Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md).
    -   When you delete an invoice line record, you’re prompted with a pop-up message to confirm the deletion of an invoice line record removes its associated cost allocation record.
    -   When you select allocation type as cost center for the first record and save the changes, the subsequent records also will inherit the same allocation type.
6.  Select **Save**.


## Result

The cost allocation form is added to the invoice line.

**Parent Topic:**[Invoice cost allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/invoice-line-cost-allocation.md)

**Related topics**  


[Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-invoice-processing.md)

[Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-workspace.md)

[Use ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/using-now-assist-apo.md)

[Invoice processing cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/working-with-ingestion-cases.md)

[Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md)

