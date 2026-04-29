---
title: Customize overlay time series on the floor map
description: Update the decision table to configure the time duration option on the floor map. You can view the operational data of the datacenters for a selected time range as overlay on the floor map in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Overlays on floor map, Configure, Telecommunications Network Inventory]
---

# Customize overlay time series on the floor map

Update the decision table to configure the time duration option on the floor map. You can view the operational data of the datacenters for a selected time range as overlay on the floor map in the Telecommunications Network Inventory application.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

You can modify the time duration option on the floor map by configuring the **TNI Data Center Time Duration Configuration** decision table. The operational data for the time series you selected appears as a colored layer on the floor map.

For the time duration configuration, if the time value is set to one second, the latest metric value is retrieved from the ClothoDB. For all other time durations, the system returns the average metric value over the specified duration.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Select the **TNI Data Center Time Duration Configuration** decision table.

3.  Select **Create Draft**.

4.  Do one of the following.

<table id="choicetable_tyg_2bt_nfc"><thead><tr><th align="left" id="d46499e101">

Action

</th><th align="left" id="d46499e104">

Details

</th></tr></thead><tbody><tr><td id="d46499e110">

**Add time duration for a new overlay**

</td><td>

1.  Select the **Type** field.
2.  Select **Choice list source** as **Create new choice list**.
3.  Type new overlay name in the **Choices** field.
4.  Select **Add**.
5.  Select **Done**.
6.  In the Condition section, add the time duration values for the new overlay.


</td></tr><tr><td id="d46499e159">

**Edit time duration for an existing overlay**

</td><td>

In the Time Duration Value section, edit the time duration for the overlay that you want to customize.

</td></tr><tr><td id="d46499e168">

**Delete time duration for an overlay**

</td><td>

1.  Select the Menu Type field.
2.  Select the delete icon \(![Delete Icon.](../../../common/image/icon-delete-trashcan.png)\) to delete an overlay.
3.  In the Condition section, delete the corresponding time duration rows.


</td></tr></tbody>
</table>5.  Select **Publish**.


## Result

Customized time duration options are available on the floor map.

**Parent Topic:**[Configuring overlays on floor map](../concept/configure-overlays-floor-map.md)

