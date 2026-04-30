---
title: Complete the Asset ship task for a requested Device as a Service \(DaaS\) asset
description: After you prepare the DaaS asset that you picked for an inbound asset order line, complete the Asset ship task for it by shipping it to the customer that it is requested for.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-10-20"
reading_time_minutes: 3
breadcrumb: [Completing an inbound asset order, Managing inbound asset orders for requested DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Complete the Asset ship task for a requested Device as a Service \(DaaS\) asset

After you prepare the DaaS asset that you picked for an inbound asset order line, complete the Asset ship task for it by shipping it to the customer that it is requested for.

## Before you begin

Before you can begin the Asset ship task, you must complete the preceding Asset prepare task by preparing the asset for shipment. For detailed instructions, see [Complete the Asset prepare task for a requested Device as a Service \(DaaS\) asset](prepare-picked-daas-asset-inbound-asset-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_wwt_xxs_1hc"><thead><tr><th align="left" id="d163397e91">

Navigation option

</th><th align="left" id="d163397e94">

Procedure

</th></tr></thead><tbody><tr><td id="d163397e100">

**Provider inbound asset order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order**.
2.  From the list of available inbound asset orders, select the order that you want to complete.
3.  On the inbound asset order record, select the **Inbound asset order lines** tab.
4.  From the list of available inbound asset order lines, select the order line that you want to ship an asset for.

**Note:** You must select an order line that you have already completed the Asset prepare task for.

5.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d163397e144">

**Provider inbound asset order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order line**.
2.  From the list of available inbound asset order lines, select the order line that you want to ship an asset for.

**Note:** You must select an order line that you have already completed the Asset prepare task for.

3.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d163397e179">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Asset ship task that you want to complete.

4.  On the **Details** tab of the Asset ship task, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Due date|Date and time at which you must complete the task.|
    |Shipping carrier|Shipping carrier through which you are shipping the asset. For example, **DHL**.|
    |Ship from|Geographic location that you are shipping the asset from.|
    |Ship date|Date and time at which you shipped the asset.|
    |Assignment group|Group that the task is assigned to.|
    |Assigned to|User who the task is assigned to.|
    |Tracking number|Tracking number that you can use to track the status and location of the asset shipment.|
    |Ship to|Geographic location that you are shipping to asset to.|
    |Short description|Brief description of the task.|
    |Description|Detailed description of the task.|
    |Work notes \(Private\)|Notes about the task that are visible to all users within your organization.|

5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Asset ship task closes with an updated state of Closed Complete.
-   A corresponding shipment record is automatically created for the asset shipment. A reference to the shipment record is populated in the **Shipment order** field of the Asset ship task. You can view and manage the shipment record from the Shipments list of the Asset operations view. For detailed instructions, see [View and add enterprise asset shipments](view-enterprise-asset-shipments.md).
-   A corresponding Receive task is automatically generated.

## What to do next

Complete the corresponding Receive task by verifying that the customer successfully received the shipped asset. For detailed instructions, see [Complete the Receive task for a requested Device as a Service \(DaaS\) asset](receive-shipped-daas-asset-inbound-asset-order.md).

**Parent Topic:**[Completing an inbound asset order for requested Device as a Service \(DaaS\) assets](../concept/completing-inbound-asset-order-daas-assets.md)

