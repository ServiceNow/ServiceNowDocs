---
title: Invoice cost allocation
description: Cost allocation is a process of identifying and allocating the costs across different cost centers or ledger accounts. Accounts Payable specialists allocate invoice line cost across multiple cost centers or ledger accounts for accurate cost analysis and invoice processing.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2024-09-25"
reading_time_minutes: 2
breadcrumb: [Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice cost allocation

Cost allocation is a process of identifying and allocating the costs across different cost centers or ledger accounts. Accounts Payable specialists allocate invoice line cost across multiple cost centers or ledger accounts for accurate cost analysis and invoice processing.

Accounts Payable specialists can allocate invoice cost in the following ways:

-   Cost allocated at purchase order level-
    -   When the invoice line is matched with the purchase order line and the invoice moves to PO matching completed status, then the cost allocation related to the purchase order line is copied to the invoice line. Any existing cost allocation record is overridden.
    -   When you change the invoice type from PO to non-PO invoice, you're prompted with a warning message to confirm that updating the invoice type restarts invoice processing, closes any open exceptions and deletes any cost allocations associated with the invoice. Upon confirmation, the cost allocation record is deleted.
-   Manual cost allocation- add cost allocation at invoice line level. For more information on manual cost allocation, see [Create invoice cost allocation manually](../task/create-invoice-cost-allocation.md).

Accounts Payable specialists can allocate invoice line cost by:

-   Quantity
-   Quantity percentage
-   Amount
-   Amount percentage

For more information on cost allocation, see [Allocations](https://www.servicenow.com/docs/access?context=c_Allocations&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

-   You can create a new invoice line record and cost allocation record only when the invoice is in draft state and exception found state.
-   During cost allocation, you must confirm that the total allocated quantity or amount across different cost centers or ledger accounts must be equal to the invoice line quantity or subtotal, or else invoice cost allocation exception occurs.
-   Approval rules are configured by the approval engine that directs the invoices to cost center owners for approvals. For more information on approvals, see [Invoice approvals](invoice-approvals.md).
-   Invoices approved by cost center managers are pushed to ERP for posting. For more information on invoice outbound cost allocation, see [Outbound cost allocation staging table](../reference/outbound-cost-allocation-table.md).

-   **[Create invoice cost allocation manually](../task/create-invoice-cost-allocation.md)**  
Manually allocate invoice line cost across multiple cost centers.

**Parent Topic:**[Create an invoice manually](../task/create-invoice.md)

