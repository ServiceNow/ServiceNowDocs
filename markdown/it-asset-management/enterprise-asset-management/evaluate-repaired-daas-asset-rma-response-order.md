---
title: Complete the Evaluate asset task for a defective Device as a Service DaaS asset
description: After you repair a defective DaaS asset, complete the Evaluate asset task by evaluating the asset and determining if it can be redeployed.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Completing an RMA response order, Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Complete the Evaluate asset task for a defective Device as a Service DaaS asset

After you repair a defective DaaS asset, complete the Evaluate asset task by evaluating the asset and determining if it can be redeployed.

## Before you begin

Before you can begin the Evaluate asset task, you must complete the preceding Repair asset task by repairing the asset. For detailed instructions, see [Complete the Repair asset task for a defective Device as a Service DaaS asset](repair-daas-asset-rma-response-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_lxc_pcp_bhc"><thead><tr><th align="left" id="d127570e91">

Navigation option

</th><th align="left" id="d127570e94">

Procedure

</th></tr></thead><tbody><tr><td id="d127570e100">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to complete.
3.  On the RMA response order record, select the **RMA response order lines** tab.
4.  From the list of available RMA response order lines, select the order line that you want to evaluate the repaired asset for.

**Note:** You must select an order line that you have already completed the Repair asset task for.

5.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d127570e144">

**Provider RMA response order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.
2.  From the list of available RMA response order lines, select the order line that you want to evaluate the repaired asset for.

**Note:** You must select an order line that you have already completed the Repair asset task for.

3.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d127570e179">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Evaluate asset task that you want to complete.

4.  On the **Details** tab of the Evaluate asset task, fill in the fields.

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

Result of the evaluation. Select one of the following options:-   **Redeployable**: The repair was successful, so the asset can be redeployed.
-   **To be disposed**: The repair was unsuccessful, so the asset must be disposed of.


</td></tr><tr><td>

Issue identified

</td><td>

Reason that the repair was unsuccessful. Fill in this field only if you set the **Evaluation result** field to **To be disposed**.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the task that are visible to all users within your organization.

</td></tr></tbody>
</table>5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Evaluate asset task closes with an updated state of Closed Complete.
-   If you set the **Evaluation result** field to **Redeployable** and you performed an on-site repair, the RMA response order line moves to the Completed stage. The customer can redeploy the asset at any time.
-   If you set the **Evaluation result** field to **Redeployable** and you performed an off-site repair, a corresponding Ship task is automatically generated.

## What to do next

-   If you set the **Evaluation result** field to **Redeployable** and you performed an off-site repair, complete the corresponding Ship task by shipping the repaired asset back to the customer so that it can be redeployed. For detailed instructions, see [Complete the Ship task for a defective Device as a Service DaaS asset](ship-daas-asset-rma-response-order.md).
-   If you set the **Repair result** field to **Unrepairable**, the customer must dispose of the asset. For detailed instructions, see [Create a disposal order in the Enterprise Asset Workspace](create-eamdisposal-order.md).

**Parent Topic:**[Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md)

