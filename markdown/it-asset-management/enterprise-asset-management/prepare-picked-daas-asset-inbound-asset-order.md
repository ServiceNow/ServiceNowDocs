---
title: Complete the Asset prepare task for a requested Device as a Service \(DaaS\) asset
description: Before you ship the DaaS asset that you picked for an inbound asset order line, complete the Asset prepare task for it by completing any necessary pre-shipment checklists and by inspecting it for defects.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-10-20"
reading_time_minutes: 3
breadcrumb: [Completing an inbound asset order, Managing inbound asset orders for requested DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Complete the Asset prepare task for a requested Device as a Service \(DaaS\) asset

Before you ship the DaaS asset that you picked for an inbound asset order line, complete the Asset prepare task for it by completing any necessary pre-shipment checklists and by inspecting it for defects.

## Before you begin

Before you can begin the Asset prepare task, you must complete the preceding Asset pick task by picking the asset from the stockroom that the provider asset manager specifies. For detailed instructions, see [Complete the Asset pick task for a requested Device as a Service \(DaaS\) asset](pick-selected-daas-asset-inbound-asset-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_wwt_xxs_1hc"><thead><tr><th align="left" id="d300094e91">

Navigation option

</th><th align="left" id="d300094e94">

Procedure

</th></tr></thead><tbody><tr><td id="d300094e100">

**Provider inbound asset order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset inbound order**.
2.  From the list of available inbound asset orders, select the order that you want to complete.
3.  On the inbound asset order record, select the **Inbound asset order lines** tab.
4.  From the list of available inbound asset order lines, select the order line that you want to prepare an asset for.

**Note:** You must select an order line that you have already completed the Asset pick task for.

5.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d300094e144">

**Provider inbound asset order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order line**.
2.  From the list of available inbound asset order lines, select the order line that you want to prepare an asset for.

**Note:** You must select an order line that you have already completed the Asset pick task for.

3.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d300094e179">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Asset prepare task that you want to complete.

4.  On the **Details** tab of the Asset prepare task, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Due date|Date and time at which you must complete the task.|
    |Stockroom|Stockroom that the asset is located in.|
    |Assignment group|Group that the task is assigned to.|
    |Assigned to|User who the task is assigned to.|
    |Short description|Brief description of the task.|
    |Description|Detailed description of the task.|
    |Work notes \(Private\)|Notes about the task that are visible to all users within your organization.|

5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Asset prepare task closes with an updated state of Closed Complete.
-   A corresponding Asset ship task is automatically generated.

## What to do next

Complete the corresponding Asset ship task by shipping the prepared asset to the customer that the asset is requested for. For detailed instructions, see [Complete the Asset ship task for a requested Device as a Service \(DaaS\) asset](ship-prepared-daas-asset-inbound-asset-order.md).

**Parent Topic:**[Completing an inbound asset order for requested Device as a Service \(DaaS\) assets](../concept/completing-inbound-asset-order-daas-assets.md)

