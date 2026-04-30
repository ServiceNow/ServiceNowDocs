---
title: Customize a map source level
description: A map source configures data to be displayed in a map report. Customize existing map sources according to your needs.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Map report administration, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Customize a map source level

A map source configures data to be displayed in a map report. Customize existing map sources according to your needs.

## Before you begin

Role required: report\_admin or admin

## About this task

**Note:** A set of predefined map sources and maps are available by default. Use these predefined objects whenever possible. If you need a map source that does not exist, generate it automatically using **Generate map source levels** link on the map source form, then customize it.You can automatically generate map source levels only for map sources that reference the location table. These map sources have a field that ends in `.location`.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Map Sources**.

2.  Open the map source whose level you want to customize, then navigate down to the appropriate level using the **Map Sources** related lists.

    For example, click the level 1 map source name to reopen the Map Source form with the level 2 map source in the related list, and so on.

3.  Modify these fields as appropriate.

<table id="table_njp_mdw_y5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the map source. Include the level in the names of map source levels. For example, Incident by location - level 2.

</td></tr><tr><td>

Table

</td><td>

The same table is used throughout a map source hierarchy, and is specified in the top-level map source.

</td></tr><tr><td>

Field

</td><td>

Select the field whose data you want to display on the map. You can dot walk to other fields. Select a field that is one level more granular than the map you want to display the data on. For example, imagine you are configuring data for a level 1 map source that is displayed on the world map. Because the data for countries are displayed on the world map, select **Location Country**. Similarly, if you are configuring data to display on a map of Germany or the United States, select **Location State / Province**.

**Note:** The city label is the most granular level able to be displayed when drilling down into a map report. For example: If you want to report on various site locations within a city, and define the bottom-level map source field to include location.name, the map report displays the multiple locations as the corresponding city labels. As a result, reporting on multiple locations which have the same location.city value results in displaying multiple map dots with the same label, but with different aggregated values, and which drill down to different locations.

 Most map sources use a field on the Location table.

</td></tr><tr><td>

Level

</td><td>

Select a hierarchy level for this map source. You can have a maximum of four levels. Each map source level corresponds to a drill level on the map hierarchy, and these levels much match. Each level must exist in a hierarchy only once.

</td></tr><tr><td>

Active

</td><td>

Clear this check box to make this map source unavailable when creating map reports.

</td></tr></tbody>
</table>4.  In the **Data transformation** section, modify these fields as appropriate.

<table id="table_wxt_3dg_1v"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data

</td><td>

Select how to use data in this map source. -   **Use data on table**: Use the data in the ServiceNow platform without transforming it. Select this option when the data already matches the JSON key values that you are mapping to.
-   **Use mapping**: Transform that data so it matches the JSON key values that you are mapping to. For geographical map sources that use the hc-key geoJSON key, always select this option.
-   **Use longitude and latitude**: Use latitude and longitude coordinates to plot your data. Always select this option for the bottom map level, such as level 3. Ensure that your data has latitude and longitude values.

**Warning:** Because the **Use longitude and latitude** option disables heatmap and drilling for maps using this map source, select this option only on map source levels that are the bottom level in a hierarchy.

</td></tr><tr><td>

Use these mappings

</td><td>

If you selected **Use mapping**, select a mapping group to use. A mapping group is a collection of key-value pair mappings that transform data. To review the mappings in a mapping group, go to the Locations Mappings \[sys\_report\_map\_source\_mapping\] table.For example, if you are transforming field value **USA** to hc-key value **us**, select **Country mappings**, which contains the relevant key-value pair mapping.

</td></tr></tbody>
</table>5.  In the **JSON key** section, select a JSON key to connect the map source data to maps.

    Geographical maps typically use hc-key.

    Every report map has a JSON definition. Select one JSON key-value pair to map the data to. The data to appear on the map must match the JSON key values. So the key that you select determines whether you must transform your data with the settings in the **How to use data** section. All default platform maps and mappings use the [geoJSON](http://geojson.org/) hc-key and ISO 3166 standard values. For custom maps, you can enter a different JSON key.

6.  Click **Update**.


**Parent Topic:**[Map report administration](../concept/c_AdministeringMapReports.md)

**Related topics**  


[Map report objects](../concept/c_MapReportObjects.md)

[Automatically generate a map source hierarchy](t_AutoGenerateMapSourceHierarchy.md)

[Create a key-value pair mapping](t_CreateKeyValuePairMapping.md)

[Create a map](t_CreateAMap.md#)

