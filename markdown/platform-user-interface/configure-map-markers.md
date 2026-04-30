---
title: Create a map marker
description: Add a map marker icon and define the click behavior to differentiate between data on your Map Page using the Classic Environmentlis.Select a relative or absolute URL for a map marker icon to display a data item on the Map Page, and determine the map marker priority on the Map Page.Define the click actions for your Map Page marker. Click actions enable you to define what happens when you click a map marker on your Map Page.Choose a Map Page where you want to apply your map marker.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create an advanced Map Page, Map pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a map marker

Add a map marker icon and define the click behavior to differentiate between data on your Map Page using the Classic Environmentlis.

## Before you begin

Set up a [map data item](configure-map-data-items.md) before you accomplish this task.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Coordinate Definitions**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for your map coordinate definition.|
    |Type|Type of map coordinate definition. Select **Field**, which uses the Classic Environment \(lists and forms\), or **Script**.|
    |Table|Table for the condition. For example, incident \[incident\].|
    |Latitude field|Latitude field to define map coordinates. Select**Location**, then **Latitude**.|
    |Longitude field|Longitude field to define map coordinates. Select **Location**, then **Longitude**.|
    |Application|Optional application scope for your map coordinate definition, if other than Global.|

4.  Click **Submit**.

5.  Navigate to **System Map Page** &gt; **Map Markers**.

6.  Click **New**.

7.  On the form, fill in the fields.

<table id="table_tgn_5ht_tjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your map marker.

</td></tr><tr><td>

Data item

</td><td>

Data item for your map marker. Select the map data item that you previously configured.

</td></tr><tr><td>

Coordinate definition

</td><td>

Coordinate definitions for your map marker. Select the map coordinate definition that you previously configured.

</td></tr><tr><td>

Map Marker Icons

</td><td>

M2M map marker icons record. Set up map marker icons, or create new ones.**Note:** Complete all the steps to set up map marker icons.

</td></tr><tr><td>

Map Marker Click Actions

</td><td>

M2M map marker click actions record. Select map marker click actions, or create new ones. **Note:** Complete all the steps to set up map marker click actions.

</td></tr><tr><td>

Application

</td><td>

Optional application scope for your map marker, if other than Global.

</td></tr></tbody>
</table>8.  Click the menu icon \(![Menu icon](../../workspace/image/menu-icon.png)\) and select **Save**.


## What to do next

Set up map marker icons and map marker click actions to finish configuring map markers.

**Parent Topic:**[Create an advanced Map Page](create-advanced-map-page.md)

## Set up map marker icons

Select a relative or absolute URL for a map marker icon to display a data item on the Map Page, and determine the map marker priority on the Map Page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Marker Icons**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for your map marker icon.|
    |Level|Marker priority on your Map Page. When multiple markers share coordinates, the lowest level marker is displayed on your Map Page.|
    |Application|Optional application scope for you map marker icon, if other than Global.|
    |Single icon URL|Icon for a single data item from a map coordinate on your Map Page. Select a relative or absolute link.|
    |Co-located icon URL|Icon for multiple data items from a map coordinate on your Map Page. Select a relative or absolute link.|
    |Scripted condition|Optional scripting for map markers.|

4.  Click **Submit**.

5.  Navigate to **System Map Page** &gt; **Map Markers**.

6.  Select your map page marker.

7.  In the **Map Marker Icons** field, double-click the record and click the search icon \(![Search icon](../image/QueryIcon.png)\).

8.  Select your map marker icon, then click the check mark icon \(![Check mark icon](../image/CheckMark.png)\).

9.  Click the menu icon \(![Menu icon](../../workspace/image/menu-icon.png)\) and select **Save**.


### What to do next

Continue to the next task to [define map marker click actions](configure-map-markers.md#).

## Define map marker click actions

Define the click actions for your Map Page marker. Click actions enable you to define what happens when you click a map marker on your Map Page.

### Before you begin

Role required: admin

### About this task

Select a dialog box that displays form details, or script your own click actions.

### Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Marker Click Actions**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the map marker click action.|
    |Action type|Action type for the click action. Select **Display dialog form** or **Script**.|
    |Title|Title for the map marker click action. The title is displayed on the dialog form on your Map Page.|
    |Application|Optional application scope for your map marker click action, if other than Global.|
    |Form View|Form view used for the dialog box UI on your Map Page.|

4.  Click **Submit**.

5.  Navigate to **System Map Page** &gt; **Map Markers**.

6.  Select your Map Page marker.

7.  In the **Map Marker Click Actions** field, double-click the record and click the search icon \(![Search icon](../image/QueryIcon.png)\).

8.  Select your map marker click action, then click the check mark icon \(![Check mark icon](../image/CheckMark.png)\).

9.  Click the menu icon \(![Menu icon](../../workspace/image/menu-icon.png)\) and select **Save**.


### What to do next

Continue to the next task to complete your [map marker setup](configure-map-markers.md#).

## Select map markers

Choose a Map Page where you want to apply your map marker.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Pages**.

2.  Select your Map Page.

3.  In the **Map Page Markers** field, double-click the record and click the search icon \(![Search icon](../image/QueryIcon.png)\).

4.  Select your map marker, then click the check mark icon \(![Check mark icon](../image/CheckMark.png)\).

5.  Click the menu icon \(![Menu icon](../../workspace/image/menu-icon.png)\) and select **Save**.


### What to do next

You've set up a map marker. Click **Try it** on the Map Pages form to ensure that your map marker is set up correctly. After that, create a map filter to show the map markers that you want to see on your Map Page.

**Note:** If data is not available, map markers don't show.

