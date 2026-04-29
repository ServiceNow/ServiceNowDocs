---
title: Complete the Schedule task for a defective Device as a Service DaaS asset
description: If you want to perform an on-site repair or replacement for a defective DaaS asset, complete the Schedule task for the asset by scheduling a visit to the customer site.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Completing an RMA response order, Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Complete the Schedule task for a defective Device as a Service DaaS asset

If you want to perform an on-site repair or replacement for a defective DaaS asset, complete the Schedule task for the asset by scheduling a visit to the customer site.

## Before you begin

Before you can begin the Schedule task, you must complete the preceding RMA assessment task by assessing the asset and selecting the option to perform an on-site repair or replacement. For detailed instructions, see [Complete the RMA assessment task for a defective Device as a Service DaaS asset](assess-daas-asset-rma-response-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_lxc_pcp_bhc"><thead><tr><th align="left" id="d317224e91">

Navigation option

</th><th align="left" id="d317224e94">

Procedure

</th></tr></thead><tbody><tr><td id="d317224e100">

**Provider RMA response order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order**.
2.  From the list of available RMA response orders, select the order that you want to complete.
3.  On the RMA response order record, select the **RMA response order lines** tab.
4.  From the list of available RMA response order lines, select the order line that you want to schedule a customer site visit for.

**Note:** You must select an order line that you have already completed the RMA assessment task for.

5.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d317224e144">

**Provider RMA response order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider RMA response order line**.
2.  From the list of available RMA response order lines, select the order line that you want to schedule a customer site visit for.

**Note:** You must select an order line that you have already completed the RMA assessment task for.

3.  On the RMA response order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d317224e179">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Schedule task that you want to complete.

4.  On the **Details** tab of the Schedule task, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Due date|Date and time at which you must complete the task.|
    |Scheduled date|Date and time at which you plan to visit the customer site.|
    |Assignment group|Group that the task is assigned to.|
    |Assigned to|User who the task is assigned to.|
    |Short description|Brief description of the task.|
    |Description|Detailed description of the task.|
    |Work notes|Notes about the task that are visible to all users within your organization.|

5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Schedule task closes with an updated state of Closed Complete.
-   A corresponding Evaluate RMA asset task is automatically generated.

## What to do next

Complete the corresponding Evaluate RMA asset task by going to the customer site and evaluating the asset. For detailed instructions, see [Complete the Evaluate RMA asset task for a defective Device as a Service DaaS asset](evaluate-daas-asset-rma-response-order.md).

**Parent Topic:**[Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets](../concept/completing-rma-response-order-daas-assets.md)

