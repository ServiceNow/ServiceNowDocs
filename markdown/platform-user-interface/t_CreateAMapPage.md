---
title: Create a map page
description: Your ServiceNow instance provides several default map pages. You can also create custom map pages with the script examples described in this page.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Map pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a map page

Your ServiceNow instance provides several default map pages. You can also create custom map pages with the script examples described in this page.

## Before you begin

Role required: admin

## About this task

The default map page record displays critical incidents on a Google map page.

## Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Pages**.

2.  Click **New**.

3.  Complete the form using the fields in the table.

<table id="table_fdj_pzt_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name to identify the map.

</td></tr><tr><td>

Center map on

</td><td>

Enter the location for centering the map using the decimal form of latitude and longitude. For example, to center the map on the statue of liberty, enter `40.689865, -74.045235`.

</td></tr><tr><td>

Initial zoom

</td><td>

Set the zoom level of the map on opening.

</td></tr><tr><td>

Refresh on zoom

</td><td>

Enable or disable to refresh map on zoom.

</td></tr><tr><td>

Use advanced configuration

</td><td>

Select to configure a map with lists and forms. The script hides and M2M forms display to configure your map.**Note:** Advanced configuration does not support mobile.

</td></tr><tr><td>

Application

</td><td>

Select an application scope for the map.

</td></tr><tr><td>

Controls size

</td><td>

Select whether the Google navigation icons on the map should be large or small.

</td></tr><tr><td>

Type

</td><td>

Select a map background style: **Satellite**, **Hybrid**, **Normal**, or **Terrain**.

</td></tr><tr><td>

Type selection

</td><td>

Select which type of Google icons to display on the map: **Buttons** or **Menu**.

</td></tr><tr><td>

Map overview

</td><td>

Enable or disable a wide view map window for navigation.

</td></tr><tr><td>

Show device location

</td><td>

Enable or disable to show device locations.

</td></tr><tr><td>

Script

</td><td>

Create a script to define the type of data to display on this map. For more information, see [Scripting for map pages](../reference/scripting-for-map-pages.md).

</td></tr></tbody>
</table>4.  Save the record.


**Parent Topic:**[Map pages](../concept/c_MapPages.md)

**Related topics**  


[Set up Google Maps API](set-up-google-maps-api.md)

[Create a map page module](create-map-page-module.md)

[Create an advanced Map Page](create-advanced-map-page.md)

[Set map application scope](set-map-application-scope.md)

[Create a smartphone map page module](t_CreateASmartphoneMapPageModule.md)

[Scripting for map pages](../reference/scripting-for-map-pages.md)

