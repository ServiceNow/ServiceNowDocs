---
title: Cost allocations
description: Cost allocation defines how to allocate the payment for a particular purchase line. Costs can be allocated towards a cost center, employee credit, or payroll payments.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Purchase lines, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Cost allocations

Cost allocation defines how to allocate the payment for a particular purchase line. Costs can be allocated towards a cost center, employee credit, or payroll payments.

**Note:** Shipping and tax costs are excluded from cost allocation calculations.

For more information about modifying PRs and POs while preserving cost allocations across multiple cost centers, see [Editing purchase requisitions and orders with cost allocation adjustments](../concept/edit-purchase-cost-allocation.md).

The key fields for a cost allocation are as follows:

<table id="table_txc_t2p_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase line

</td><td>

Purchase line associated with this allocation.

</td></tr><tr><td>

Allocation type

</td><td>

Specifies how the cost is allocated. For example, **Cost center**, **Employee credit**, or **Payroll**.

</td></tr><tr><td>

Cost owner

</td><td>

User who incurs the cost of this allocated transaction amount.

</td></tr><tr><td>

Cost center

</td><td>

Cost center that incurs the cost of this allocated transaction amount.

</td></tr><tr><td>

Employee credit

</td><td>

Reference to the employee credit to which this cost allocation is made.This field is visible only if the allocation type is set to **Employee Credit**.

</td></tr><tr><td>

Terms accepted on

</td><td>

Date and time at which the cost owner has accepted the terms and conditions of the organization to withhold the payroll.This field is visible only if the allocation type is set to **Payroll**.

</td></tr><tr><td>

Number of payments selected

</td><td>

Number of payments that the cost owner selected to pay back for a subsidized purchase.This field is visible only if the allocation type is set to **Payroll**.

</td></tr><tr><td>

Allocate by

</td><td>

Determines if the cost allocation is made by amount or percentage.

</td></tr><tr><td>

Allocation amount

</td><td>

Amount of the cost allocated.

</td></tr><tr><td>

Allocation percentage

</td><td>

Percentage of the cost allocated.This field is visible only if the allocation type is set to **Percentage**.

</td></tr></tbody>
</table>If a purchase line is created:

-   From the ShoppingHub catalog, the cost allocation is created from the payment method that the employee selects during checkout. The employee can define the cost center to allocate to, and can split the allocation amongst multiple cost centers, as required. Employee credits and paycheck payments also result in the creation of a cost allocation.
-   When an employee submits an off-catalog request from the I need to submit a quote flow, and selects a cost center that is not their default cost center, the selected cost center gets populated in the Cost Allocation table associated to the purchase requisition line. The employee can define the cost center to allocate to, but the allocation is 100% to that cost center, and can't be split.

**Parent Topic:**[Purchase lines](purchase-lines.md)

