---
title: Invoice cost allocation
description: Cost allocation distributes invoice line costs across multiple cost centers or ledger accounts to ensure accurate financial reporting and proper expense tracking in Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-line-cost-allocation.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice processing, cost allocation, GL coding]
breadcrumb: [Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice cost allocation

Cost allocation distributes invoice line costs across multiple cost centers or ledger accounts to ensure accurate financial reporting and proper expense tracking in Accounts Payable Operations.

Accounts Payable specialists can allocate invoice cost in the following ways:

-   Cost allocated at purchase order level-
    -   When the invoice line is matched with the purchase order line and the invoice moves to PO matching completed status, then the cost allocation related to the purchase order line is copied to the invoice line. Any existing cost allocation record is overridden.
    -   When you change the invoice type from PO to non-PO invoice, you're prompted with a warning message to confirm that updating the invoice type restarts invoice processing, closes any open exceptions and deletes any cost allocations associated with the invoice. Upon confirmation, the cost allocation record is deleted.
-   Manual cost allocation- add cost allocation at invoice line level. When cost is split across multiple cost centers, the cost center field on the invoice line becomes read-only and allows one type of allocation type in cost allocations For more information on manual cost allocation, see [Create invoice cost allocation manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-cost-allocation.md).

Accounts Payable specialists can allocate invoice line cost by:

-   Quantity
-   Quantity percentage
-   Amount
-   Amount percentage.
    -   You can create a new invoice line record and cost allocation record only when the invoice is in draft state and exception found state.
    -   During cost allocation, you must confirm that the total allocated quantity or amount across different cost centers or ledger accounts must be equal to the invoice line quantity or subtotal, or else invoice cost allocation exception occurs.
    -   Approval rules are configured by the approval engine that directs the invoices to cost center owners for approvals. For more information on approvals, see [Invoice approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-approvals.md).
    -   Invoices approved by cost center managers are pushed to ERP for posting. For more information on invoice outbound cost allocation, see [Outbound cost allocation staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/outbound-cost-allocation-table.md).

-   **[Create invoice cost allocation manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-cost-allocation.md)**  
Manually allocate invoice line cost across multiple cost centers.
-   **[Distribution set in Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/distribution-sets-in-apo.md)**  
Distribution sets in Accounts Payable Operations use predefined rules and templates to automate cost allocation for invoice lines across cost centers and GL accounts.
-   **[Allocate costs using distribution set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/allocate-cost-distribution-set.md)**  
Define a distribution set to split cost allocations automatically for invoice lines with allocation type as cost center or general ledger account.

**Parent Topic:**[Create an invoice manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice.md)

