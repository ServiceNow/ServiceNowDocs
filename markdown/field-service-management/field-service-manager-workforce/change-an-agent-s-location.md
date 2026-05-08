---
title: Change map marker location in the Territory Planning console
description: Update the location of your map markers for a dynamic and accurate visual representation of your data entities on the map.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing territories and agents, Managing workforce, Use, Field Service Management]
---

# Change map marker location in the Territory Planning console

Update the location of your map markers for a dynamic and accurate visual representation of your data entities on the map.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## About this task

You can move the map marker icons from the current location to the new location only when the `Enable location change on map` field is selected and a valid `Script` is provided while creating the marker layer overlays. For more information, see [Create a marker layer overlay](../concept/configuring-map-overlay.md#).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  Edit location for marker overlay data items.

<table id="choicetable_j1m_5b2_2yb"><thead><tr><th align="left" id="d52246e101">

To

</th><th align="left" id="d52246e104">

Do the following

</th></tr></thead><tbody><tr><td id="d52246e110">

**Edit location of a single icon map marker**

</td><td>

-   Select the desired map marker icon on the map.
-   The data item card appears in the contextual side panel.
-   Click the **More actions** icon \(![More actions icon.](../image/more_actions.png)\) and select **Edit location**.

**Note:**

You can move the map marker icon from the current location to the new location only when the `Enable location change on map` field is selected and a valid `Script` is provided while creating the marker layer overlays. For more information, see [Create a marker layer overlay](../concept/configuring-map-overlay.md#).

-   Drag and drop the map marker to the desired location or enter the address manually in the **New Location** field.


</td></tr><tr><td id="d52246e165">

**Edit location of all items in a co-located marker data item**

</td><td>

-   Select the desired co-located map marker icon.
-   The list of data item cards appear in the contextual side panel.
-   Select the data item cards you wanted to change location for.
-   Click **Edit location**.
-   Drag and drop the map marker to the desired location or enter the address manually in the **New Location** field.


</td></tr></tbody>
</table>    As you drag and drop the map markers to the new location, the system populates the address details automatically in the **New Location** field for the data items.

3.  Select **Update**.


## Result

The following snapshots illustrate the process of changing data item locations when selecting a single map marker or a co-located map marker icon.![GIF displaying the process of changing the map overlay data item's location.](../image/csp.gif)

