---
title: Complete the Receive task for a requested Device as a Service \(DaaS\) asset
description: After you ship the DaaS asset that you prepared for an inbound asset order line, complete the Receive task for it by verifying that the customer received it successfully.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-10-20"
reading_time_minutes: 2
breadcrumb: [Completing an inbound asset order, Managing inbound asset orders for requested DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Complete the Receive task for a requested Device as a Service \(DaaS\) asset

After you ship the DaaS asset that you prepared for an inbound asset order line, complete the Receive task for it by verifying that the customer received it successfully.

## Before you begin

Before you can begin the Receive task, you must complete the preceding Asset ship task by shipping the asset. For detailed instructions, see [Complete the Asset ship task for a requested Device as a Service \(DaaS\) asset](ship-prepared-daas-asset-inbound-asset-order.md).

Role required: sn\_eam\_provider.provider\_asset\_technician

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  Open the Asset tasks list.

<table id="choicetable_wwt_xxs_1hc"><thead><tr><th align="left" id="d117380e91">

Navigation option

</th><th align="left" id="d117380e94">

Procedure

</th></tr></thead><tbody><tr><td id="d117380e100">

**Provider inbound asset order**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order**.
2.  From the list of available inbound asset orders, select the order that you want to complete.
3.  On the inbound asset order record, select the **Inbound asset order lines** tab.
4.  From the list of available inbound asset order lines, select the order line that you want to verify the asset receipt for.

**Note:** You must select an order line that you have already completed the Asset ship task for.

5.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d117380e144">

**Provider inbound asset order line**

</td><td>

1.  From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider inbound asset order line**.
2.  From the list of available inbound asset order lines, select the order line that you want to verify the asset receipt for.

**Note:** You must select an order line that you have already completed the Asset ship task for.

3.  On the inbound asset order line record, select the **Asset tasks** tab.


</td></tr><tr><td id="d117380e179">

**Provider asset tasks**

</td><td>

From the navigation menu of the Asset operations view, navigate to **Provider** &gt; **Provider asset tasks**.

</td></tr></tbody>
</table>3.  From the list of available tasks, select the task number for the Receive task that you want to complete.

4.  On the **Details** tab of the Receive task, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Due date|Date and time at which you must complete the task.|
    |Asset|Asset that was shipped to the customer.|
    |Asset received|Option that indicates if the customer received the asset. Select either **Yes** or **No**.|
    |Assignment group|Group that the task is assigned to.|
    |Assigned to|User who the task is assigned to.|
    |Short description|Brief description of the task.|
    |Description|Detailed description of the task.|
    |Work notes|Notes about the task that are visible to all users within your organization.|

5.  Select **Close Task**.

    **Note:** If you want to save your progress and close the task at a later time, select **Save** instead. You can return to the task at any time.


## Result

-   The Receive task closes with an updated state of Closed Complete.
-   The inbound asset order line moves to the Completed stage.
-   The state of the asset changes to In Transit.

**Parent Topic:**[Completing an inbound asset order for requested Device as a Service \(DaaS\) assets](../concept/completing-inbound-asset-order-daas-assets.md)

