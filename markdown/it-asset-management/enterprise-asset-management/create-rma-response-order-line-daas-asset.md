---
title: Create a Return Merchandise Authorization \(RMA\) response order line for a defective Device as a Service \(DaaS\) asset
description: Create an RMA response order line for each defective DaaS asset that you want to repair or replace through an RMA response order. Use each order line to track and manage the tasks that you must complete to repair or replace the given asset.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Create a Return Merchandise Authorization \(RMA\) response order line for a defective Device as a Service \(DaaS\) asset

Create an RMA response order line for each defective DaaS asset that you want to repair or replace through an RMA response order. Use each order line to track and manage the tasks that you must complete to repair or replace the given asset.

## Before you begin

Role required: sn\_eam\_provider.provider\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the RMA response order lines list.

<table id="choicetable_my1_vjg_bhc"><thead><tr><th align="left" id="d209053e78">

Navigation option

</th><th align="left" id="d209053e81">

Procedure

</th></tr></thead><tbody><tr><td id="d209053e87">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to create an RMA response order line for.
3.  On the RMA response order record, select the **RMA response order lines** tab.


</td></tr><tr><td id="d209053e120">

**Provider RMA response order line**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.

</td></tr></tbody>
</table>3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_fmv_3l4_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Model of the asset that you want to repair or replace.

</td></tr><tr><td>

Assigned to

</td><td>

User who is assigned to repair or replace the specified asset.

</td></tr><tr><td>

Asset

</td><td>

Asset that you want to repair or replace.**Note:** The list of available assets is automatically filtered to display only the assets that meet the following criteria:

-   The asset is associated with the model specified in the **Model** field.
-   The **DaaS asset** option is enabled on the corresponding asset record.
-   The **DaaS account** field on the corresponding asset record matches the DaaS account specified in the associated RMA response order.


</td></tr></tbody>
</table>5.  Select **Save**.


## Result

-   The RMA response order line is added to the associated RMA response order.
-   An RMA assessment task is automatically generated for the RMA response order line.

## What to do next

Perform all tasks that are required for completing the RMA response order line so that you can complete and close the associated RMA response order. For detailed instructions, see [Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md).

**Parent Topic:**[Managing Return Merchandise Authorization \(RMA\) response orders for defective Device as a Service \(DaaS\) assets](../concept/managing-rma-response-orders-daas-assets.md)

