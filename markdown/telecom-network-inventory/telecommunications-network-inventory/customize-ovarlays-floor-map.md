---
title: Customize overlays on the floor map
description: Update the decision table to configure the overlays appearing on the floor map. You can view the operational data of the datacenters as overlay on the floor map in the Telecommunications Network Inventory application.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-06-03"
reading_time_minutes: 2
breadcrumb: [Configuring overlays on floor map, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Customize overlays on the floor map

Update the decision table to configure the overlays appearing on the floor map. You can view the operational data of the datacenters as overlay on the floor map in the Telecommunications Network Inventory application.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

When you select an overlay and time duration on the floor map, the system uses **TNI Data Center Overlay Configuration** decision table to determine the corresponding operational data. The decision table pulls the average metric value for each Configuration Item \(CI\) over that duration from ClothoDB. Based on the value, the system assigns the predetermined color code. The floor map updates with these colors, so you can quickly see the status of operational status of each CI.

For example, when you select **Temperature** overlay and time duration as **Past 3 hours**, the system automatically collects the data from ClothoBD. If the current time is 9:00 PM, the system queries data from 6:00 PM to 9:00 PM. Clotho returns the average metric value for each CI over that duration. This average is then evaluated against the decision table to determine the corresponding range and associated color code. Finally, each CI is visually updated on the floor map using that color, enabling you to understand the health of the datacenters.

You can edit the overlay option in the floor map by configuring the decision table. You can add or delete an overlay option and also set up the color options.

**Note:** Decision table inputs should remain unedited. You can add or update decision table rows to customize colors or overlay ranges as needed.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Select the **TNI Data Center Overlay Configuration** decision table.

3.  Select **Create Draft**.

4.  Do one of the following.

<table id="choicetable_tyg_2bt_nfc"><thead><tr><th align="left" id="d38797e116">

Action

</th><th align="left" id="d38797e119">

Details

</th></tr></thead><tbody><tr><td id="d38797e125">

**Add a new overlay**

</td><td>

1.  Select the **Type** field.
2.  Select **Choice list source** as **Create new choice list**.
3.  Type new overlay name in the **Choices** field.
4.  Select **Add**.
5.  Select **Done**.
6.  In the Condition section, add the metric values and color code.


</td></tr><tr><td id="d38797e174">

**Edit an existing overlay**

</td><td>

1.  Select the **Type** field.
2.  Edit the overlay name that you want to update in the **Choices** field.
3.  Select **Done**.
4.  In the Condition section, edit the metric values and color code.


</td></tr><tr><td id="d38797e207">

**Delete an overlay**

</td><td>

1.  Select the **Type** field.
2.  Select the delete icon \(![Delete Icon.](../../../common/image/icon-delete-trashcan.png)\) to delete an overlay.
3.  In the Condition section, delete the corresponding overlay rows.


</td></tr></tbody>
</table>5.  Select **Publish**.


## Result

Customized overlay options are displayed on the floor map, and the color legend updates accordingly.

## What to do next

Set up time duration for the operational data. To learn more, see [Customize overlay time series on the floor map](customize-overlay-time-series-floor-map.md).

**Parent Topic:**[Configuring overlays on floor map](../concept/configure-overlays-floor-map.md)

**Related topics**  


[Capacity management](../concept/capacity-management-reporting.md)

[Time series metrics for datacenter](../reference/time-series-metrics.md)

