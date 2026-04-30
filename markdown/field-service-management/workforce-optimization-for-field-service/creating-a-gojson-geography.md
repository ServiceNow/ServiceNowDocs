---
title: Creating a GeoJSON geography
description: Create a GeoJSON geography by importing GeoJSON co-ordinates or drawing shapes directly on the map.Create a geography of type GeoJSON.Draw boundaries on the map to define your geographic areas and create GeoJSON geographies. These geographies not only give you a clear visual on the map but also used task scheduling.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Creating geographies, Configuring Field Service Territory Planning, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Creating a GeoJSON geography

Create a GeoJSON geography by importing GeoJSON co-ordinates or drawing shapes directly on the map.

## Create a GeoJSON geography

Create a geography of type GeoJSON.

### Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

### About this task

Use GeoJSON geography type to accommodate scenarios where detailed geo-spatial information is available externally, enabling organizations to incorporate diverse geographic datasets into the planning processes.

**Note:** For effective task assignments using Schedule Optimization, it is recommended to use consistent shapes \(like polygons or circles\) and avoid overlapping or intersecting geographies to ensure accurate results.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Geography**.

2.  In the **Territory Geographies** page, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the geography.|
    |Geography type|Select **GeoJSON**.|
    |GeoJSON|Use the GeoJSON format for encoding variety of geographical data structures. GeoJSON supports the geometry types such as polygon, multi-polygon, and circle.|

4.  Select **Submit**.

    The geography of type GeoJSON is created based on the given coordinates.


### Result

After creating a GeoJSON geography, connect it to a territory for work order management; the associated territory will be listed in the **Territories** related list when you open the geography record. The geography of GeoJSON type appears visually on the map when its territory is selected in the Territory Planning console.

### What to do next

Link the geography to a territory. For more information, see [Create a Field Service territory](../task/create-territories-territory-planning-console.md).

## Create a GeoJSON geography in Territory Planning console

Draw boundaries on the map to define your geographic areas and create GeoJSON geographies. These geographies not only give you a clear visual on the map but also used task scheduling.

### Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner

### About this task

Allows you to interactively draw shapes such as polygons or circles directly on the map, streamlining the process of creating territories for effective task assignment. If necessary, you can create a multi polygon based geography by drawing multiple polygons on the map. For example, if the geographic area for a territory comprises water and land, you can select multiple land areas spread across the water body to define a territory geography.

**Note:** For effective task assignments using Schedule Optimization, it is recommended to use consistent shapes \(like polygons or circles\) and avoid overlapping or intersecting geographies to ensure accurate results.

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  In the Territories panel, select **Create Territory**.

    The Create New Territory page appears.

3.  In the Geography field, select the New Geography for Territory icon \(![New Geography for Territory icon.](../image/EditWidgetButton.png)\) to draw a geography.

4.  Select the drawing method.

    -   To draw a geography using an existing territory, choose **Draw using territory** and select the desired territory from the list in the Territories panel.
    -   To search for an area on the map, by entering a location in the Search address bar, select **Draw on map**.
    **Note:** To create a geography based on the presence of resources \(Agents, Crews, or Assets\), select the desired resources from the overlay options displayed on the map.

5.  Select the drawing tool.

    -   To draw a boundary area or multiple areas, use the polygon shape icon \(![Draw a shape icon.](../image/Polygon-shape.png)\).
    -   To define a geography with a specific radius, use the circle shape icon \(![Draw a circle icon.](../image/Circle-shape.png)\).
6.  In the Name field, enter the name for the geography.

    A GeoJSON script is automatically generated.

7.  Click **Save**.

    The GeoJSON geography is created based on the selected area on the map.


### Result

After creating a GeoJSON geography, connect it to a territory for work order management; the associated territory will be listed in the **Territories** related list when you open the geography record. The geography appears visually on the map when its territory is selected in the Territory Planning console.

### What to do next

Link the geography to a territory. For more information, see [Create a Field Service territory](../task/create-territories-territory-planning-console.md).

