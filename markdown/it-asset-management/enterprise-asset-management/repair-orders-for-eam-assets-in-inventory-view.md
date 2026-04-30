---
title: Create repair orders for enterprise assets in the Inventory view
description: Request repair of enterprise assets that are defective or pending repair by creating a repair order in the Inventory view of Enterprise Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request repair of defective enterprise assets, Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Create repair orders for enterprise assets in the Inventory view

Request repair of enterprise assets that are defective or pending repair by creating a repair order in the Inventory view of Enterprise Asset Workspace.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager or sn\_eam.enterprise\_asset\_technician.

## About this task

When you create a repair order from the Inventory view, you must explicitly create a repair order line for the asset that you want to get repaired.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Create a Repair order.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        **Note:** The following fields are optional:

        -   **Assignment group**
        -   **Assigned to**
        -   **Due date**
        -   **Work note**
<table id="table_nkm_bzd_lbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Stockroom

</td><td>

Stockroom that has assets to be repaired.This field is required.

</td></tr><tr><td>

Assignment group

</td><td>

Assignment group to which you want to assign the repair order.

</td></tr><tr><td>

Assigned to

</td><td>

Person from the assignment group who is primarily responsible for the Repair order.

</td></tr><tr><td>

Due date

</td><td>

Date by which the defective enterprise assets should be repaired.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the repair order.

</td></tr></tbody>
</table>    3.  Select **Save**.

    -   A repair order that's in the **Draft** stage is created.
    -   The **Repair order lines** tab is displayed next to the **Details** tab of the repair order.
4.  Add repair order lines to the repair order.

    1.  Select the **Repair order lines** tab.

    2.  Select **Add**.

    3.  In the **Add assets** dialog box, select the assets and then select **Add**.

        **Note:** You can add child assets of a pallet asset to the repair order. The asset that you added to the repair order is removed from the pallet automatically.

    For each asset that you added, a repair order line that's in the **Troubleshoot** stage is created.

5.  Select **Save**.


**Parent Topic:**[Request repair of defective enterprise assets](../concept/request-repair-defective-eam-assets.md)

