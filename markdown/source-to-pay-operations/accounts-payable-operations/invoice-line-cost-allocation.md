---
title: Invoice cost allocation
description: Cost allocation is a process of identifying and allocating the costs across different cost centers or ledger accounts. Accounts Payable specialists allocate invoice line cost across multiple cost centers or ledger accounts for accurate cost analysis and invoice processing.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice cost allocation

Cost allocation is a process of identifying and allocating the costs across different cost centers or ledger accounts. Accounts Payable specialists allocate invoice line cost across multiple cost centers or ledger accounts for accurate cost analysis and invoice processing.

Accounts Payable specialists can allocate invoice cost in the following ways:

-   Cost allocated at purchase order level-
    -   When the invoice line is matched with the purchase order line and the invoice moves to PO matching completed status, then the cost allocation related to the purchase order line is copied to the invoice line. Any existing cost allocation record is overridden.
    -   When you change the invoice type from PO to non-PO invoice, you're prompted with a warning message to confirm that updating the invoice type restarts invoice processing, closes any open exceptions and deletes any cost allocations associated with the invoice. Upon confirmation, the cost allocation record is deleted.
-   Manual cost allocation- add cost allocation at invoice line level. When cost is split across multiple cost centers, the cost center field on the invoice line becomes read-only and allows one type of allocation type in cost allocations For more information on manual cost allocation, see [Create invoice cost allocation manually](../task/create-invoice-cost-allocation.md).

Accounts Payable specialists can allocate invoice line cost by:

-   Quantity
-   Quantity percentage
-   Amount
-   Amount percentage

For more information on cost allocation, see .

-   You can create a new invoice line record and cost allocation record only when the invoice is in draft state and exception found state.
-   During cost allocation, you must confirm that the total allocated quantity or amount across different cost centers or ledger accounts must be equal to the invoice line quantity or subtotal, or else invoice cost allocation exception occurs.
-   Approval rules are configured by the approval engine that directs the invoices to cost center owners for approvals. For more information on approvals, see [Invoice approvals](invoice-approvals.md).
-   Distribution set is added for cost allocation type. For more information on how distribution set is added for cost type, see [Distribution set in Accounts Payable Operations](distribution-sets-in-apo.md).
-   Distribution sets automate the creation of cost allocations for invoice lines by applying pre-defined rules or filters and distribution lines included during their setup.
-   Manual Selection: AP specialists can manually select a distribution set while creating cost allocation records for an invoice line, enabling bulk automation as per defined distribution lines.
-   For PO invoices, cost allocations can be copied from the PO. If invoice attributes meet the default rule or filter criteria in distribution set, distribution lines will also apply.
-   The template feature in a distribution set automatically creates cost allocation records for invoice lines without amounts. AP specialists can then manually allocate costs across cost centers or general ledger accounts.
-   Any over or under-allocation will be flagged during the exception stage.

BEnefits of distribution set in cost allocation records are:

-   Reduces risk of cost allocation errors.
-   Speeds up invoice processing by minimizing manual work for AP specialists.

-   **[Create invoice cost allocation manually](../task/create-invoice-cost-allocation.md)**  
Manually allocate invoice line cost across multiple cost centers.
-   **[Distribution set in Accounts Payable Operations](distribution-sets-in-apo.md)**  
Distribution set in Accounts Payable Operations is a collection of predefined rules, including template, designed to automate the allocation of costs for invoice lines across cost centers and GL accounts.
-   **[Allocate costs using distribution set](../task/allocate-cost-distribution-set.md)**  
Define a distribution set to split cost allocations automatically for invoice lines with allocation type as cost center or general ledger account.

**Parent Topic:**[Create an invoice manually](../task/create-invoice.md)

**Related topics**  


[Accounts Payable Invoice Processing](acc-pay-invoice-processing.md)

[Invoice Case Management](acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](acc-pay-workspace.md)

[Accounts Payable Operations integration with Document Intelligence](apo-docintel-integration.md)

[Using Now Assist for Accounts Payable Operations \(APO\)](using-now-assist-apo.md)

[Using Supplier Collaboration Portal in APO](using-supplier-collaboration-portal.md)

[Invoice processing cases](working-with-ingestion-cases.md)

[Distribution set in Accounts Payable Operations](distribution-sets-in-apo.md)

