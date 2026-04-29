---
title: Complete the RMA assessment task for a defective Device as a Service DaaS asset
description: Complete the RMA assessment task for a defective DaaS asset by assessing the asset and determining the action that you want to take on it. You can choose to repair it, replace it, or reject the associated RMA request.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Completing an RMA response order, Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Complete the RMA assessment task for a defective Device as a Service DaaS asset

Complete the RMA assessment task for a defective DaaS asset by assessing the asset and determining the action that you want to take on it. You can choose to repair it, replace it, or reject the associated RMA request.

## Before you begin

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_lxc_pcp_bhc"><thead><tr><th align="left" id="d253924e78">

Navigation option

</th><th align="left" id="d253924e81">

Procedure

</th></tr></thead><tbody><tr><td id="d253924e87">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to complete.
3.  On the RMA response order record, select the **RMA response order lines** tab.
4.  From the list of available RMA response order lines, select the order line that you want to assess the asset for.
5.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d253924e129">

**Provider RMA response order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.
2.  From the list of available RMA response order lines, select the order line that you want to assess the asset for.
3.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d253924e162">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the RMA assessment task that you want to complete.

4.  On the **Details** tab of the RMA assessment task, fill in the fields.

<table id="table_lsg_3dp_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment action

</td><td>

Action that you want to take on the asset. Select one of the following options:-   **On site**: Option to repair or replace the asset at the customer site.
-   **Off site**: Option to repair or replace the asset at your organization's site.
-   **Denied**: Option to reject the RMA request.


</td></tr><tr><td>

Assignment group

</td><td>

Group that the task is assigned to.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The RMA assessment task closes with an updated state of Closed Complete.
-   If you set the **Assessment action** field to **On site**, a corresponding Schedule task is automatically generated.
-   If you set the **Assessment action** field to **Off site**, a corresponding Ship task is automatically generated.
-   If you set the **Assessment action** field to **Denied**, the associated RMA response order line moves to the Rejected stage.

## What to do next

-   If you set the **Assessment action** field to **On site**, complete the corresponding Schedule task by scheduling a visit to the customer site. For detailed instructions, see [Complete the Schedule task for a defective Device as a Service DaaS asset](schedule-customer-visit-rma-response-order.md).
-   If you set the **Assessment action** field to **Off site**, complete the corresponding Ship task by having the customer ship the asset to you. For detailed instructions, see [Complete the Ship task for a defective Device as a Service DaaS asset](ship-daas-asset-rma-response-order.md).

**Parent Topic:**[Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md)

