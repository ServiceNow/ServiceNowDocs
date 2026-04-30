---
title: Complete the Repair asset task for a defective Device as a Service DaaS asset
description: Complete the Repair asset task for a defective DaaS asset by repairing the asset either on-site or off-site.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 3
breadcrumb: [Completing an RMA response order, Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Complete the Repair asset task for a defective Device as a Service DaaS asset

Complete the Repair asset task for a defective DaaS asset by repairing the asset either on-site or off-site.

## Before you begin

Before you can begin the Repair asset task, you must complete the preceding Evaluate RMA asset task by evaluating the asset and indicating that it is repairable. For detailed instructions, see [Complete the Evaluate RMA asset task for a defective Device as a Service DaaS asset](evaluate-daas-asset-rma-response-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_lxc_pcp_bhc"><thead><tr><th align="left" id="d117989e91">

Navigation option

</th><th align="left" id="d117989e94">

Procedure

</th></tr></thead><tbody><tr><td id="d117989e100">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to complete.
3.  On the RMA response order record, select the **RMA response order lines** tab.
4.  From the list of available RMA response order lines, select the order line that you want to repair the asset for.

**Note:** You must select an order line that you have already completed the Evaluate RMA asset task for.

5.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d117989e144">

**Provider RMA response order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.
2.  From the list of available RMA response order lines, select the order line that you want to repair the asset for.

**Note:** You must select an order line that you have already completed the Evaluate RMA asset task for.

3.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d117989e179">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Repair asset task that you want to complete.

4.  On the **Details** tab of the Repair asset task, fill in the fields.

<table id="table_lsg_3dp_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

Group that the task is assigned to.

</td></tr><tr><td>

Repair result

</td><td>

Result of the repair. Select one of the following options:-   **Repaired**: The asset was repaired.
-   **Unrepairable**: The asset is unrepairable and must be replaced.


</td></tr><tr><td>

Issue identified

</td><td>

Reason that the asset is unrepairable. Fill in this field only if you set the **Repair result** field to **Unrepairable**.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Repair asset task closes with an updated state of Closed Complete.
-   If you set the **Repair result** field to **Repaired**, a corresponding Evaluate asset task is automatically generated.
-   If you set the **Repair result** field to **Unrepairable**, a corresponding Ship task is automatically generated.

## What to do next

-   If you set the **Repair result** field to **Repaired**, complete the corresponding Evaluate asset task by evaluating the repaired asset and determining if it can be redeployed. For detailed instructions, see [Complete the Evaluate asset task for a defective Device as a Service DaaS asset](evaluate-repaired-daas-asset-rma-response-order.md).
-   If you set the **Repair result** field to **Unrepairable**, complete the corresponding Ship task by having the customer ship the asset to you for replacement. For detailed instructions, see [Complete the Ship task for a defective Device as a Service DaaS asset](ship-daas-asset-rma-response-order.md).

**Parent Topic:**[Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md)

