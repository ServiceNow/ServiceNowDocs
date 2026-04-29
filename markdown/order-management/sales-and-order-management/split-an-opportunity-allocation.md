---
title: Split opportunity allocation
description: Split an allocation row to divide its credit between two contributors while keeping, for example, the same product family and effective date.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Managing allocations, Opportunity Management, Lead and opportunity apps, Use, Sales and Order Management]
---

# Split opportunity allocation

Split an allocation row to divide its credit between two contributors while keeping, for example, the same product family and effective date.

## Before you begin

Role required: sn\_opty\_mgmt\_core.opportunity\_allocation\_writer

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Opportunity** &gt; **All**, open the opportunity record, and select the **Allocations** tab.

3.  Select **Manage Allocations**.

4.  Select the allocation type that contains the row you want to split.

5.  Select **Split allocation** icon on that row.

    A new row is inserted immediately below the original. The grouping/dimensions related fields are copied from the original row. All other fields are blank.

6.  Update the Percentage \(or Amount\) on both the original row and the new row so that together they reflect the intended split — for example, 70% and 30%.

    **Note:** If the Require full allocation property is enabled, the combined percentages for the allocation type must total 100% before saving.

7.  Fill in the row ﬁelds:

    -   Team Member: Select the opportunity team member.
    -   Territory: Select one among the active sales territory from the active territory model.

        **Note:** When a team member is selected, the territory list includes only territories in which the member is an active territory member.

    -   Allocation Percentage: Allocation percentage assigned to the team member for their allocation.
    -   Allocation Amount: Monetary value of the allocation.
    -   Reason: Additional notes.
8.  Select **Save**.

    **Note:** Users with the Account Executive role in Sales Territory Membership or Opportunity Team Member have create, split, and update access to Revenue-based allocations. Overlay allocations are read-only for these users.

    The allocation is split into two rows. Both rows are saved and displayed in the Allocations tab under the relevant allocation type.


**Parent Topic:**[Managing allocations](../concept/manage-allocations.md)

