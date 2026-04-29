---
title: Add or edit opportunity allocations
description: Use the allocations configurator to add new allocation rows, edit existing ones, or split an allocation across multiple contributors.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 2
breadcrumb: [Managing allocations, Opportunity Management, Lead and opportunity apps, Use, Sales and Order Management]
---

# Add or edit opportunity allocations

Use the allocations configurator to add new allocation rows, edit existing ones, or split an allocation across multiple contributors.

## Before you begin

Role required: sn\_opty\_mgmt\_core.opportunity\_allocation\_writer

## About this task

The configurator displays active allocation types in the left pane. Each type shows its current row count, for example, Revenue \(2\). You can switch between types and make changes to any of them. All changes across all types are saved or discarded together when you select Save or Discard changes.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Opportunity** &gt; **All**, open the opportunity record, and select the Allocations tab.

3.  Select **Manage Allocations**.

4.  In the left pane, select an allocation type - for example, Revenue.

5.  Select **Add allocation**.

    A new blank row is added at the bottom of the list. The Effective Date is pre-filled with the opportunity's estimated close date.

6.  Fill in the row fields:

    -   Team Member: Select the opportunity team member.
    -   Territory: Select one among the active sales territory from the active territory model.

        **Note:** When a team member is selected, the territory list includes only territories in which the member is an active territory member.

    -   Product Offering Family: High-level product grouped under which the product offering belongs to. Shows the product offering family for products added to opportunity lines.
    -   Allocation Percentage: Allocation percentage assigned to the team member for their allocation.
    -   Allocation Amount: Monetary value of the allocation.
    -   Effective Date: Date on which the allocation becomes effective for crediting. Used for sales forecasting.
    -   Reason: Additional notes.
    **Note:**

    -   The percentage and amount fields are interdependent; a change to either value triggers automatic recalculation of the other.
    -   If the Require full allocation property is enabled, the combined percentages for the allocation type must total 100% before saving.
    -   When a type is associated with multiple dimensions, all dimensions are mandatory fields in the configurator.
7.  Select any cell in a row to edit and update its value.

8.  Select **Save** to commit all changes across all allocation types.

    **Note:** **Save** and **Discard changes** are only enabled when there are unsaved changes. If you navigate away with unsaved changes, you are prompted to save, discard, or continue editing.

    The allocation rows are saved. The Allocations tab count updates to reflect the new total.

9.  Select **Delete allocation** to delete the allocation.


**Parent Topic:**[Managing allocations](../concept/manage-allocations.md)

