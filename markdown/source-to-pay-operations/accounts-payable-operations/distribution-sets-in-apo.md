---
title: Distribution set in Accounts Payable Operations
description: Distribution set in Accounts Payable Operations is a collection of predefined rules, including template, designed to automate the allocation of costs for invoice lines across cost centers and GL accounts.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-11-07"
reading_time_minutes: 2
breadcrumb: [Invoice cost allocation, Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Distribution set in Accounts Payable Operations

Distribution set in Accounts Payable Operations is a collection of predefined rules, including template, designed to automate the allocation of costs for invoice lines across cost centers and GL accounts.

By applying a distribution set, Accounts Payable teams can efficiently generate cost allocation records automatically, eliminating the need for manual cost splitting for each invoice line.

The key features of the distribution set are:

-   AP Admin can define distribution sets and add distribution lines with varying percentages across cost centers or general ledger accounts.
-   Distribution sets can be end-dated by specifying an effective-to-date. After expiration, they’ll no longer be automatically applied to invoice lines according to the invoice date.
-   A distribution set can be marked as a template to automate creation of cost allocation records without amounts.
-   The template feature in the distribution set automatically generates cost allocation records for invoice lines, and also enables AP specialists to divide costs by allocation type, such as cost center or general ledger account. Any over or under allocation will be flagged during the exception stage.
-   For non-template-based distribution sets, the AP administrator must input allocation percentage so that the total sums to 100% and the distribution set becomes auto-active. If the total doesn't sum to 100%, then the distribution set remains inactive.
-   An AP administrator is able to establish filters or rules that automatically assign distribution sets throughout the invoice processing workflow, thereby eliminating the requirement for manual selection.
-   AP specialist can manually select a distribution set during the processing of an invoice.
-   Reduces the risk of cost allocation errors.
-   Distribution sets apply to both PO and Non-PO invoices.
-   Speeds up the invoice processing by reducing manual work by AP specialists.

    The workflow of the distribution set is shown below:


![Distribution set](../image/distribution-set.png)

The key features of distribution lines are:

-   Distribution lines can be associated with either cost centers or general ledger accounts; however, they can’t be linked to both at the same time.
-   Duplicate distribution lines aren’t enabled.
-   Allocation type is restricted to amount percentage for each distribution line.
-   When the distribution set is set as a template, the percentage column is read-only, and AP specialists can manually allocate costs later.

**Parent Topic:**[Invoice cost allocation](invoice-line-cost-allocation.md)

