---
title: Complete the Asset pick task for a requested Device as a Service \(DaaS\) asset
description: Complete the Asset pick task for a requested DaaS asset by picking the asset that a provider asset manager selected for an inbound asset order line. You must pick the asset from the stockroom that the provider asset manager specified when selecting the asset.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-10-20"
reading_time_minutes: 3
breadcrumb: [Completing an inbound asset order, Managing inbound asset orders for requested DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Complete the Asset pick task for a requested Device as a Service \(DaaS\) asset

Complete the Asset pick task for a requested DaaS asset by picking the asset that a provider asset manager selected for an inbound asset order line. You must pick the asset from the stockroom that the provider asset manager specified when selecting the asset.

## Before you begin

Before you can begin the Asset pick task, a provider asset manager must complete the preceding Asset selection task by selecting an asset for the inbound asset order line. For detailed instructions, see [Complete the Asset selection task for a requested Device as a Service \(DaaS\) asset](select-daas-asset-inbound-asset-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_wwt_xxs_1hc"><thead><tr><th align="left" id="d313908e91">

Navigation option

</th><th align="left" id="d313908e94">

Procedure

</th></tr></thead><tbody><tr><td id="d313908e100">

**Provider inbound asset order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order**.
2.  From the list of available inbound asset orders, select the order that you want to complete.
3.  On the inbound asset order record, select the **Inbound asset order lines** tab.
4.  From the list of available inbound asset order lines, select the order line that you want to pick an asset for.

**Note:** You must select an order line that a provider asset manager has already completed the Asset selection task for.

5.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d313908e144">

**Provider inbound asset order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order line**.
2.  From the list of available inbound asset order lines, select the order line that you want to pick an asset for.

**Note:** You must select an order line that a provider asset manager has already completed the Asset selection task for.

3.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d313908e179">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available asset tasks, select the task number for the Asset pick task that you want to complete.

4.  On the **Details** tab of the Asset pick task, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Asset pick task|
    |Assignment group|Group that the task is assigned to.|
    |Assigned to|User who the task is assigned to.|
    |Due date|Date and time at which you must complete the task.|
    |Drop off location|Location where the asset must be delivered.|
    |Notes|
    |Short description|Brief description of the task.|
    |Description|Detailed description of the task.|
    |Work notes|Notes about the task that are visible to all users within your organization.|

5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Asset pick task closes with an updated state of Closed Complete.
-   A corresponding Asset prepare task is automatically generated.

## What to do next

Complete the corresponding Asset prepare task by preparing the picked asset for shipment. For detailed instructions, see [Complete the Asset prepare task for a requested Device as a Service \(DaaS\) asset](prepare-picked-daas-asset-inbound-asset-order.md).

**Parent Topic:**[Completing an inbound asset order for requested Device as a Service \(DaaS\) assets](../concept/completing-inbound-asset-order-daas-assets.md)

