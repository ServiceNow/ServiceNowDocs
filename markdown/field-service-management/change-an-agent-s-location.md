---
title: Change map marker location in the Territory Planning console
description: Update the location of your map markers for a dynamic and accurate visual representation of your data entities on the map.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/field-service-management/change-an-agent-s-location.html
release: xanadu
product: Field Service Management
classification: field-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Field Service Territory Planning Console, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Change map marker location in the Territory Planning console

Update the location of your map markers for a dynamic and accurate visual representation of your data entities on the map.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## About this task

You can move the map marker icons from the current location to the new location only when the `Enable location change on map` field is selected and a valid `Script` is provided while creating the marker layer overlays. For more information, see [Create a marker layer overlay](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/configuring-map-overlay.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  Edit location for marker overlay data items.

<table id="choicetable_j1m_5b2_2yb"><thead><tr><th align="left" id="d37108e92">

To

</th><th align="left" id="d37108e95">

Do the following

</th></tr></thead><tbody><tr><td id="d37108e101">

**Edit location of a single icon map marker**

</td><td>

-   Select the desired map marker icon on the map.
-   The data item card appears in the contextual side panel.
-   Click the **More actions** icon \(\[Omitted image "more\_actions.png"\] Alt text: More actions icon.\) and select **Edit location**.

**Note:**

You can move the map marker icon from the current location to the new location only when the `Enable location change on map` field is selected and a valid `Script` is provided while creating the marker layer overlays. For more information, see [Create a marker layer overlay](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/configuring-map-overlay.md).

-   Drag and drop the map marker to the desired location or enter the address manually in the **New Location** field.


</td></tr><tr><td id="d37108e156">

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

The following snapshots illustrate the process of changing data item locations when selecting a single map marker or a co-located map marker icon.\[Omitted image "csp.gif"\] Alt text: GIF displaying the process of changing the map overlay data item's location.

**Parent Topic:**[Using Field Service Territory Planning Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/using-territory-planning-console.md)

