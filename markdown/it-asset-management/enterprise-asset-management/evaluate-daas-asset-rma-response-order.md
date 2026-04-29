---
title: Complete the Evaluate RMA asset task for a defective Device as a Service DaaS asset
description: Complete the Evaluate RMA asset task for a defective DaaS asset by evaluating the asset and determining whether you want to repair or replace it.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Completing an RMA response order, Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Complete the Evaluate RMA asset task for a defective Device as a Service DaaS asset

Complete the Evaluate RMA asset task for a defective DaaS asset by evaluating the asset and determining whether you want to repair or replace it.

## Before you begin

Before you can begin the Evaluate RMA asset task, you must complete the preceding task.

-   If you are performing an on-site repair or replacement, you must complete the preceding Schedule task by scheduling a visit to the customer site. For detailed instructions, see [Complete the Schedule task for a defective Device as a Service DaaS asset](schedule-customer-visit-rma-response-order.md).
-   If you are performing an off-site repair or replacement, you must complete the preceding Ship task by having the customer ship the asset to you. For detailed instructions, see [Complete the Receive asset task for a defective Device as a Service DaaS asset](receive-shipped-daas-asset-rma-response-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_lxc_pcp_bhc"><thead><tr><th align="left" id="d337574e112">

Navigation option

</th><th align="left" id="d337574e115">

Procedure

</th></tr></thead><tbody><tr><td id="d337574e121">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to complete.
3.  On the RMA response order record, select the **RMA response order lines** tab.
4.  From the list of available RMA response order lines, select the order line that you want to evaluate the asset for.

**Note:** If you are performing an on-site repair, you must select an order line that you have already completed the Schedule task for. If you are performing an off-site repair or replacement, you must select an order line that you have already completed the Receive asset task for.

5.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d337574e165">

**Provider RMA response order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.
2.  From the list of available RMA response order lines, select the order line that you want to evaluate the asset for.

**Note:** If you are performing an on-site repair, you must select an order line that you have already completed the Schedule task for. If you are performing an off-site repair or replacement, you must select an order line that you have already completed the Receive asset task for.

3.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d337574e200">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Evaluate RMA asset task that you want to complete.

4.  On the **Details** tab of the Evaluate RMA asset task, fill in the fields.

<table id="table_lsg_3dp_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

Group that the task is assigned to.

</td></tr><tr><td>

Evaluation result

</td><td>

Result of the evaluation. Select one of the following options:-   **Repairable**: The asset can be repaired.
-   **Replace**: The asset is unrepairable and must be replaced.


</td></tr><tr><td>

Issue identified

</td><td>

Reason that the asset is defective.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Evaluate RMA asset task closes with an updated state of Closed Complete.
-   If you set the **Evaluation result** field to **Repairable**, a corresponding Repair asset task is automatically generated for both on-site and off-site repairs.
-   If you set the **Evaluation result** field to **Replace** and you are performing an on-site replacement, a corresponding Ship task is automatically generated.
-   If you set the **Evaluation result** field to **Replace** and you are performing an off-site replacement, a corresponding inbound asset order is automatically created.

## What to do next

-   If you set the **Evaluation result** field to **Repairable**, complete the corresponding Repair asset task by repairing the asset. For detailed instructions, see [Complete the Repair asset task for a defective Device as a Service DaaS asset](repair-daas-asset-rma-response-order.md).
-   If you set the **Evaluation result** field to **Replace** and you are performing an on-site replacement, complete the corresponding Ship task by shipping the asset to your organization. For detailed instructions, see [Complete the Ship task for a defective Device as a Service DaaS asset](ship-daas-asset-rma-response-order.md).
-   If you set the **Evaluation result** field to **Replace** and you are performing an off-site replacement, complete the corresponding inbound asset order to provide the customer with a new asset. For detailed instructions, see [Completing an inbound asset order for requested Device as a Service \(DaaS\) assets](../concept/completing-inbound-asset-order-daas-assets.md).

**Parent Topic:**[Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md)

