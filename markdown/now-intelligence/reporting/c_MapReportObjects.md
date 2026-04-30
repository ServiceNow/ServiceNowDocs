---
title: Map report objects
description: Map objects define the different levels that users can drill down into on a map report and the data displayed on these levels. Admins can create and manage these objects.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Map report administration, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Map report objects

Map objects define the different levels that users can drill down into on a map report and the data displayed on these levels. Admins can create and manage these objects.

Each map report contains a map source hierarchy, which configures the data for a map level. The report also contains a map hierarchy, which defines the map drill levels. The Level field connects levels for these hierarchies. For example, the data in the Level 1 map is displayed on the Level 1 map object.

**Note:** A set of predefined map sources and maps are available by default. Use these predefined objects whenever possible. If you need a map source that does not exist, generate it automatically using **Generate map source levels** link on the map source form, then customize it.You can automatically generate map source levels only for map sources that reference the location table. These map sources have a field that ends in `.location`.

![Architecture of objects used in map reports.](../image/MapArchitecture.png)

<table id="table_dsl_3tv_y5"><thead><tr><th>

Object

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Map source

</td><td>

Defines a set of data to display on a map report. The map source that a user selects in the **Map data** field when creating a map report is actually a map source hierarchy. There is one map source level for each drill level on the map. The top map source in the hierarchy is not a level, but rather a wrapper for other hierarchy levels. Each map source contains the data for a single map hierarchy drill level, with both having the same **Level**.

 Because they both specify the data that is used for a report, a map source is similar to a report source. However, in a map source you select a field to report on instead of a table.

</td></tr><tr><td>

Map

</td><td>

The map that data is displayed on. Maps are set up in a hierarchy defined by parent-child relationships. Each hierarchy level is a drill level on the map report. A JSON definition \(geoJSON definition for geographical maps\) defines the actual map layout. Select an existing map or create a new one. You can optionally define conditions for a map, which further filters the data it displays.

</td></tr><tr><td>

Mappings

</td><td>

Transform the data in a map source to a value that can be displayed on a map. Mappings are organized into the **Countries** and **State / Province** mapping groups. During map source configuration, you select the mapping group to transform the data in that source. The mapping group that you select must match the **Field** that you have selected.

 For example, a map source that has a **Field** value of **Locations Country** would use the **Country mappings** group. A map source that has a **Field** value of **Locations State / Province** would use the **Region and state mappings** mapping group.

</td></tr></tbody>
</table>**Parent Topic:**[Map report administration](c_AdministeringMapReports.md)

**Related topics**  


[Automatically generate a map source hierarchy](../task/t_AutoGenerateMapSourceHierarchy.md)

[Customize a map source level](../task/t_CustomizeAMapSourceLevel.md)

[Create a key-value pair mapping](../task/t_CreateKeyValuePairMapping.md)

[Create a map](../task/t_CreateAMap.md#)

