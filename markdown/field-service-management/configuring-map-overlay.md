---
title: Configuring a map overlay
description: Configure a map overlay to view its corresponding data items in the territory map.Create a marker layer overlay to specify the data items associated with the markers on a map. You can set up markers for assets, locations, or points of interest.A shape layer overlay enables you to create custom shapes, such as polygons or lines, on a map. This type of overlay is useful for defining boundaries, illustrating routes, or highlighting specific geographic areas of interest.Create a heatmap to provide a visual representation of data density or intensity on a map using colors. A heatmap can help you identify areas with higher concentrations of data, highlight hotspots, and find patterns in data distribution.Create custom map marker icons for the marker type overlay.Create Info window field set to retrieve the field data from the database and display on a card when a marker is clicked on a map.Create a map overlay definition by linking the map overlay data items, info window field set, and marker icons \(in case of marker overlay\). The overlay definition appears in the map and is further used to view and filter the data on the map.Establish a link between the overlay group and overlay definition in the group usage table. This helps the overlay definition to appear in the Territory Planning console.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 19
breadcrumb: [Configuring Field Service Territory Planning Console, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Configuring a map overlay

Configure a map overlay to view its corresponding data items in the territory map.

Map overlays allow you to view data items in the context of a territory map. By setting up overlays, you can visualize data points as markers, shapes, or heatmaps on the map, providing valuable insights into spatial distribution.

## Types of Map Overlays

Supports three types of map overlay data items:

1.  Marker Layer: Represents individual data items with distinct markers on the map. Marker layers are useful for pinpointing specific assets, locations, or points of interest.
2.  Shape Layer: Allows the creation of custom shapes like polygons or lines on the map, which is valuable for defining boundaries or illustrating routes.
3.  Heatmap: Provides a visual representation of data density or intensity, helping identify areas with higher concentrations.

## Create a marker layer overlay for agents

To create a marker layer overlay specifically for agents, do the following:

1.  Add a map overlay data item for assets by linking the Agents database table.
2.  Set up map marker icons to visually identify single and multiple agents on the map.
3.  Create an info window field set to configure the fields displayed in the contextual side panel when clicking a map marker.
4.  Create an overlay definition for agents by linking the data item, map marker icons, and info window field set.
5.  Link the agents group and the agents overlay definition in the group usage table.

The following snapshot displays data related to multiple layers and heatmap in the Territory Planning console. ![Territory Planning console displaying layers information such as agents, assets, and crews and a heatmap for work order tasks.](../image/tp-console-csp.jpg)

## Viewing and filtering data

-   Use the snapshot or map view to gain insights into relevant territory information, including agents, crews, and work order tasks across territories.
-   Utilize data filter options to narrow down the displayed information based on viewport or territories.
    -   Viewport: In this view, individual markers representing each agent are prominently shown, providing a comprehensive understanding of their spatial distribution.
    -   Territory: Alternatively, the territory-based data view allows you to filter and display agents specifically associated with selected territories, providing a focused analysis of agent distribution within those areas.

## Multiple overlay selection

You can manage and control multiple map overlays. Toggle between overlays to tailor your display and optimize your mapping workflow.

## Configuration overview

The steps for configuring a map overlay are:

-   [Create a marker layer overlay](configuring-map-overlay.md#)

    Create a marker layer overlay to specify the data items associated with the markers on a map. You can set up markers for assets, locations, or points of interest.

-   [Create a shape layer overlay](configuring-map-overlay.md#)

    Create a shape layer to create custom shapes, such as polygons or lines, on a map. This type of overlay is useful for defining boundaries, illustrating routes, or highlighting specific geographic areas of interest.

-   [Create a heatmap](configuring-map-overlay.md#)

    Create a heatmap to provide a visual representation of data density or intensity on a map using colors. A heatmap can help you identify areas with higher concentrations of data, highlight hotspots, and find patterns in data distribution.

-   [Create map marker icons](configuring-map-overlay.md#)

    Create custom map marker icons for the marker type overlay to identify selected data item as either a single entity or multiple entities at the same location in the territory.

-   [Create info window field set](configuring-map-overlay.md#)

    Create Info window field set to retrieve the field data from the database and display on a card when a marker is clicked on a map.

-   [Create a map overlay definition](configuring-map-overlay.md#)

    Create a map overlay definition to link data items, info windows, and marker icons for clear visual representation on the map. This allows users to easily view and filter map data.

-   [Link overlay group and overlay definition](configuring-map-overlay.md#)

    Establish a link between the overlay group and overlay definition in the group usage table to ensure the overlay definition is displayed in the Territory Planning console.


## Create a marker layer overlay

Create a marker layer overlay to specify the data items associated with the markers on a map. You can set up markers for assets, locations, or points of interest.

### Before you begin

Role required: map\_overlay\_action\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Map Overlay** &gt; **Overlay Data items**.

2.  In the **Map Overlay Data Items** page, select **New**.

3.  On the form, fill in the fields.

<table id="table_olb_tzs_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the map overlay. For example, Assets

</td></tr><tr><td>

Application

</td><td>

Application scope of the marker layer.

</td></tr><tr><td>

Type

</td><td>

**Marker Layer**.

</td></tr><tr><td>

Table

</td><td>

Table from which you want to retrieve the data. For example, use the 'sys\_user' table to fetch agents-related data.

</td></tr><tr><td>

Advanced

</td><td>

Choose to create a marker layer either by using a customized script or filling in the predefined fields.-   To use customized script: Check this box to utilize your own script for the map overlay. This enables you to incorporate latitude, longitude, and other relevant data.
-   To enter details manually: Leave the check box unchecked to manually enter the condition, latitude, longitude, and address details.


</td></tr><tr><td>

Script

</td><td>

Customize script that aligns with your requirements. The following output format serves as a reference for the structure of the data to be used in the script. ```
[
  {
    "displayValue": "Gina Frost",
    "sysId": "01e7632ad1c30110f8773afecccd7bc3",
    "latitude": 37.4076716,
    "longitude": -121.9613086,
    "address": "Santa Clara"
  },
  {
    "displayValue": "Taylor Key",
    "sysId": "01e7632ad1c30110f8773afecccd7bd0",
    "latitude": 37.3323182,
    "longitude": -121.9745714,
    "address": "Santa Clara"
  }
]
```

</td></tr><tr><td>

Enable location change on map

</td><td>

Select to enable marker location change in the map.

</td></tr><tr><td>

Edit script

</td><td>

Customize script to update the location of the marker overlay when you drag map markers. This feature is designed for marker layers.For example, when you drag a map marker representing an agent into a new location, the script is executed and updates location in the agent's record.

</td></tr><tr><td>

Condition

</td><td>

Condition to filter the data. For example, Set Active as True to fetch only active assets. This field appears when the **Advanced** field isn’t selected.

</td></tr><tr><td>

Latitude

</td><td>

Specify latitude for the marker. For example, Location latitude of an agent. This field appears when the **Advanced** field isn’t selected.

</td></tr><tr><td>

Longitude

</td><td>

Specify the longitude for the marker. For example, Location longitude of an agent. This field appears when the **Advanced** field isn’t selected.

</td></tr><tr><td>

Address

</td><td>

Address information associated with the marker. For example, location of an agent. This field appears when the **Advanced** field isn’t selected.

</td></tr></tbody>
</table>4.  Add map marker icons to represent individual data items and visually indicate the underlying data points on the map.

    For more information, see [Create map marker icons](configuring-map-overlay.md#).

5.  Configure an info window field set to determine the fields that you want to display in a card when a map marker icon is selected.

    For more information, see [Create info window field set](configuring-map-overlay.md#).

6.  Create a map overlay definition, to link the overlay definition and data item.

    This step establishes the connection between the visual representation, such as marker icons, and the associated data item. For more information, see [Create a map overlay definition](configuring-map-overlay.md#).

7.  Link the created map overlay definition and the chosen overlay group.

    This linkage ensures that the overlay is appropriately organized and managed within the specified overlay group. For more information, see [Link overlay group and overlay definition](configuring-map-overlay.md#).

    The marker layer is created.


### Result

The following snapshot illustrates an example of marker layer representing agents in San Diego territory. Select any agent's map marker to view agent details in the right contextual side panel. ![Snapshot of agents in San Diego territory.](../image/marker-layer.png)

## Create a shape layer overlay

A shape layer overlay enables you to create custom shapes, such as polygons or lines, on a map. This type of overlay is useful for defining boundaries, illustrating routes, or highlighting specific geographic areas of interest.

### Before you begin

Role required: map\_overlay\_action\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Map Overlay** &gt; **Overlay Data items**.

2.  In the **Map Overlay Data Items** page, select **New**.

3.  On the form, fill in the fields.

<table id="table_olb_tzs_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the map overlay. For example, Linear segments

</td></tr><tr><td>

Application

</td><td>

Application scope of the shape layer.

</td></tr><tr><td>

Type

</td><td>

**Shape Layer**.

</td></tr><tr><td>

Table

</td><td>

Table from which you want to retrieve the data. For example, 'sn\_eam\_linear\_segment'. **Note:** Linear segments are accessible only when you activate the Enterprise Asset Management \(EAM\) plugin.

</td></tr><tr><td>

Advanced

</td><td>

The check box is selected by default. Indicates a script is needed to include latitude, longitude, and other relevant data for the shape layer overlay.

</td></tr><tr><td>

Script

</td><td>

Use the reference script to employ your own customized script for the map overlay. This enables you to incorporate latitude, longitude, and other relevant data. ```
[
  {
    "displayValue": "Created 2023-07-10 03:01:37",
    "sysId": "1708508093c0b51025bcba774dba106e",
    "geoJson": "{\"type\":\"FeatureCollection\",\"features\":[{\"type\":\"Feature\",\"geometry\":{\"type\":\"Polygon\",\"coordinates\":[[[110.41327466868162,-6.946524999819999],[110.41363733131837,-6.946524999819999],[110.41363733131837,-6.94688500018],[110.41327466868162,-6.94688500018],[110.41327466868162,-6.946524999819999]]]},\"properties\":{\"styles\":{\"fillColor\":\"#FF0000\",\"fillOpacity\":0.4,\"strokeWeight\":0,\"strokeColor\":\"#000000\"}}}]}"
  },
  {
    "displayValue": "Created 2023-07-10 03:06:44",
    "sysId": "1e3914c493c0b51025bcba774dba101d",
    "geoJson": "{\"type\":\"FeatureCollection\",\"features\":[{\"type\":\"Feature\",\"geometry\":{\"type\":\"Polygon\",\"coordinates\":[[[110.41258766868162,-6.946524999819999],[110.41295033131837,-6.946524999819999],[110.41295033131837,-6.94688500018],[110.41258766868162,-6.94688500018],[110.41258766868162,-6.946524999819999]]]},\"properties\":{\"styles\":{\"fillColor\":\"#FFC0CB\",\"fillOpacity\":0.4,\"strokeWeight\":0,\"strokeColor\":\"#000000\"}}}]}"
  }
]
```

</td></tr></tbody>
</table>4.  Configure an info window field set to determine the fields that you want to display in a card when a map marker icon is selected.

    For more information, see [Create info window field set](configuring-map-overlay.md#).

5.  Create a map overlay definition, you need to link the overlay definition and data item.

    This step establishes the connection between the visual representation of the shape and the associated data item. For more information, see [Create a map overlay definition](configuring-map-overlay.md#).

6.  Link the created map overlay definition and the chosen overlay group.

    This linkage ensures that the overlay is appropriately organized and managed within the specified overlay group. For more information, see [Link overlay group and overlay definition](configuring-map-overlay.md#).

    The shape layer is created.


### Result

The following snapshot illustrates an example of a shape layer representing linear segments of the San Francisco territory. Select the linear segment to view details in the right contextual side panel.

![Snapshot of Linear segments in San Francisco territory.](../image/shapes-layer.png)

## Create a heatmap

Create a heatmap to provide a visual representation of data density or intensity on a map using colors. A heatmap can help you identify areas with higher concentrations of data, highlight hotspots, and find patterns in data distribution.

### Before you begin

Role required: map\_overlay\_action\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Map Overlay** &gt; **Overlay Data items**.

2.  In the **Map Overlay Data Items** page, select **New**.

3.  On the form, fill in the fields.

<table id="table_olb_tzs_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the map overlay. For example, work order tasks.

</td></tr><tr><td>

Application

</td><td>

Application scope of the heatmap.

</td></tr><tr><td>

Type

</td><td>

Select **Heatmap**.

</td></tr><tr><td>

Table

</td><td>

Specify the table from which you want to retrieve the data. For example, use 'wm\_task' to fetch work order tasks.

</td></tr><tr><td>

Advanced

</td><td>

There are two ways to create a heatmap: using a customized script or filling in the predefined fields.-   To use customized script: Check this box to use your own script for the map overlay. This enables you to incorporate latitude, longitude, and other relevant data.
-   To enter details manually: Leave the check box unchecked to enter the condition, latitude, longitude, and address details.


</td></tr><tr><td>

Script

</td><td>

Customize script that aligns with your requirements. The following output format serves as a reference for the structure of the data to be used in the script. ```
[
  {
    "weight": 4,(optional)
    "displayValue": "WOT0010017",
    "sysId": "0793bd6847c8b51046cd016c416d43c2",
    "latitude": 25.784294,
    "longitude": -80.322654
  }
]
```

</td></tr><tr><td>

Condition

</td><td>

Condition to filter the data. For example, Set Active as True to fetch only active work order tasks. This field appears when the **Advanced** field isn’t selected.

</td></tr><tr><td>

Latitude

</td><td>

Specify latitude for heatmap. For example, Location latitude of the work order task. This field appears when the **Advanced** field isn’t selected.

</td></tr><tr><td>

Longitude

</td><td>

Specify longitude for heatmap. For example, Location longitude of the work order task. This field appears when the **Advanced** field isn’t selected.

</td></tr><tr><td>

Weight

</td><td>

Enter weight for heatmap. Determines the intensity of a data point on the heatmap. Assigning a higher weight to a data point makes it appear more prominently. This is useful for emphasizing specific data points or when adding a large amount of data at a single location for faster rendering.For example, you can have the priority field in the work order task to showcase the weight of a particular location.

**Note:** This field appears only for the heatmap and only when the **Advanced** field isn’t selected.

</td></tr></tbody>
</table>4.  Change the color gradient of the visualization using the Heatmap Gradient \(sn\_cmn\_mo.HeatmapGradient\) extension point.

    For more information, see [Extension points in Field Service Management](../reference/extension-points-field-service.md).

5.  Change the opacity level and the radius that influence the data point in the heatmap.

    For more information, see [Field Service Territory Planning console properties](../reference/territory-planning-components-fsm.md#).

6.  Create a map overlay definition, link the overlay definition and data item.

    This step establishes the connection between the visual representation of the heatmap and the associated data item. For more information, see [Create a map overlay definition](configuring-map-overlay.md#).

7.  Link the created map overlay definition and the chosen overlay group.

    This linkage ensures that the overlay is appropriately organized and managed within the specified overlay group. For more information, see [Link overlay group and overlay definition](configuring-map-overlay.md#).

8.  Select **Submit**.

    The heatmap is created.


### Result

The following example shows how agents as markers and a heatmap for work order tasks. Agents are marked on the map, and the heatmap shows task intensity. It helps you easily see agent locations and the density of work order tasks.

By using this combined approach, you can assess the spatial distribution of agents and gain insights into the workload based on the intensity of work order tasks. Select the map marker or heatmap to view the details in the right contextual side panel.

![Snapshot displaying agents and work order tasks in the map.](../image/heatmap.png).

## Create map marker icons

Create custom map marker icons for the marker type overlay.

### Before you begin

Role required: map\_overlay\_action\_admin

### About this task

You can create custom map markers and use them in the marker layer map overlay definition. Map markers identify the selected data item as single entity or multiple entities at the same location \(latitude, longitude\) in the territory. For example, create map marker icons to represent single stockroom, multiple stockrooms or a combination of multiple stockrooms and agents at a particular location.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **Map Overlay Icon**.

2.  Click **Show Form**.

    The **Map Overlay Icon** page appears.

3.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Name|Name of the map marker.|
    |Application|Select **Global** to make the marker icon available globally.|
    |Icon|Choose an appropriate icon for the map marker from the available options.|
    |Display Level|If multiple marker icons share the same coordinates, the icon with the lowest display level value will appear on the map.|
    |Highlighted Icon|Select an icon to be displayed as a highlighted marker when the user clicks on it.|

4.  Select **Submit**.

    The map marker icon is created.


### What to do next

Once the map marker icons are created, you can link them to the overlay definition to identify the data items as single entities, multiple entities, or a combination at the same location on the map. For more information, see [Create a map overlay definition](configuring-map-overlay.md#).

## Create info window field set

Create Info window field set to retrieve the field data from the database and display on a card when a marker is clicked on a map.

### Before you begin

Role required: map\_overlay\_action\_admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **Application Field Set**

2.  Click **Show Form**.

    The **Application Field Set** page appears.

3.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Name|Name of the field set. For example, Stockroom|
    |Module|Field Service Management|
    |Type|Table Fields|
    |Table name|Name of the table. For example, alm\_stockroom|

4.  Select **Submit**.

    The Application Field Set is created.

5.  Click **Show List**.

6.  Add items to the application field set.

    1.  Select the application field set.

        For example, Stockroom.

    2.  Click **New**.

    3.  Select the field name.

        For example, location.

    4.  In the **Name** field, enter name for the selected field.

        For example, Location.

    5.  In the **Order** field, enter the order of the field to appear when you click the map marker in the map.


### Result

The info window field set is created with the specified field. The values for the fields appear when you click a map marker in the map in the right contextual side panel.

### What to do next

Link the map marker icons to the overlay definition. For more information, see [Create a map overlay definition](configuring-map-overlay.md#).

## Create a map overlay definition

Create a map overlay definition by linking the map overlay data items, info window field set, and marker icons \(in case of marker overlay\). The overlay definition appears in the map and is further used to view and filter the data on the map.

### Before you begin

Role required: map\_overlay\_action\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Map Overlay** &gt; **Overlay Definitions**.

2.  In the **Map Overlay Definitions** page, click **New**.

3.  On the form, fill in the fields.

<table id="table_olb_tzs_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the map overlay definition. For example, Stockroom.

</td></tr><tr><td>

Application

</td><td>

Global

</td></tr><tr><td>

Active

</td><td>

Select to display the overlay definition in the map.

</td></tr><tr><td>

Data item

</td><td>

Contains meta data for overlays. For example, stockroom related data. For more information, see [Create a marker layer overlay](configuring-map-overlay.md#).

</td></tr><tr><td>

Single Icon Set

</td><td>

Map marker icon to identify the selected data item as a single entity. For example, if there is a single stockroom at a particular location, then the single icon set marker icon denotes there is only a single stockroom.**Note:** Appears only when the selected data item is of type marker layer.

</td></tr><tr><td>

Info Window Field Set

</td><td>

Select a field set or create a new field set by configuring the field values to appear in the right contextual panel when you click on the overlay item. For more information, see [Create info window field set](configuring-map-overlay.md#).**Note:** Appears only when the selected data item is either of type marker or shape layer.

</td></tr><tr><td>

Colocated Icon Set

</td><td>

Map marker icon to identify the selected data item as multiple entities. For example, if there are multiple stockrooms at a particular location, then the colocated icon set marker appears to denote there are multiple stockrooms.**Note:** Appears only when the selected data item is of type marker.

</td></tr></tbody>
</table>4.  Select **Submit**.


### Result

The map overlay definition is created.

### What to do next

[Link overlay group and overlay definition](configuring-map-overlay.md#)

## Link overlay group and overlay definition

Establish a link between the overlay group and overlay definition in the group usage table. This helps the overlay definition to appear in the Territory Planning console.

### Before you begin

Role required: map\_overlay\_action\_admin

### About this task

You can link the overlay group and overlay definition to any one of the following overlay groups based on where you want to view the overlay definition.

-   **FSM Territory Overlays by Territory** displays the overlay definition based on territory.
-   **FSM Territory Overlays by Viewport** displays the overlay definition based on the view port.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **Map Overlay Group Usage**.

2.  Click **Show List**.

    The **Map Overlay Group Usages** page appears.

3.  Click **New**.

4.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Group|Select the overlay group.|
    |Application|Global|
    |Overlay|Select the map overlay definition. For more information, see [Create a map overlay definition](configuring-map-overlay.md#).|
    |Active|Select the check box to ensure the overlay definition appears in map.|
    |Order|Order of the overlays to be displayed in map.|


### Result

The overlay definition appears either on the view port or territory based on the linked group usage.

