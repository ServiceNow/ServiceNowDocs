---
title: Map sources for geomap data visualizations
description: Geomap data visualizations are connected to location tables in a special map source.To use a custom location table in geomap data visualizations, define a map source that links to the table. Add more map sources at different levels of the hierarchy.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Create a geomap visualization, Data visualizations in Platform Analytics, Platform Analytics]
---

# Map sources for geomap data visualizations

Geomap data visualizations are connected to location tables in a special map source.

Map sources for geomaps are organized in map source hierarchies. All map sources that reference the same table are in the same hierarchy. A map source hierarchy consists of a parent source and up to four levels of child sources. The parent source references only the table and the child sources reference fields in the table.

By default, your instance has a map source hierarchy for geomaps that references the Location \[cmn\_location\] table. You can therefore have a Group by field on your geomap that references a field on Location. The Group by field can be at the top level of the data source table, or you can dot-walk to it. You can create additional map source hierarchies that reference custom location tables.

## Differences between map sources for data visualizations and for reports

If you’re familiar with Map reports in Core UI, you might have noticed that the map sources for geomaps are different than map sources for map reports. They’re different enough to be on different Map sources tables, sys\_report\_map\_source and viz\_map\_source. The most significant difference is in how they reference tables.

In map reports, the map source references the facts table, such as Incident \[incident\]. The map source also includes a reference field that points to the location table. Child map sources dot-walk to a field on the location table. This structure results in a separate map source hierarchy for every data table you want as a data source for a map.

![List of map sources for map reports showing facts tables.](../image/classic-map-sources.png "Map sources for map reports")

Map sources for geomaps point directly to location tables. They don’t reference facts tables. The facts table is specified only in the geomap data visualization. Thanks to this structure, you can reuse one map hierarchy for all geomaps on your instance, regardless of the data they display.

![Reusable set of map sources for all geomap data visualizations on an instance.](../image/dv-map-sources.png "Map sources for geomap data visualizations")

## Create a data visualization map source

To use a custom location table in geomap data visualizations, define a map source that links to the table. Add more map sources at different levels of the hierarchy.

### Before you begin

Role required: report\_admin, viz\_admin, pa\_admin

### About this task

### Procedure

1.  Append `viz_map_source_list.do` to your instance URL in the browser URL field.

    For example, if your instance is `https://instance.example.com`, enter `https://instance.example.com/viz_map_source_list.do`.

2.  Verify whether the location table that you want to reference is already used in a map source.

    The set of map sources that reference the same table is called a map source hierarchy.

3.  If there are no map sources that reference the desired location table, create the top-level map source for that table:

    1.  Select **New**.

        An empty Map source \[viz\_map\_source\] record opens.

    2.  Specify the following information:

        |Field|Description|
        |-----|-----------|
        |Name|Add a name for the map source. Use a descriptive name that suggests the table contents. Include this name as part of the names of all other map sources that you create in this hierarchy.|
        |Table|Select a location table that is not already being used in a data visualization map source. The table you select must also not reference a table, such as cmn\_location, that is already being used in a data visualization map source.|

    3.  Select **Submit**.

    You now have the parent map source of a new map source hierarchy. You can add more levels to the hierarchy.

4.  If a map source hierarchy for your table exists, open the map source that is one level above the map source that you want to create.

    **Note:** You can have no more than four levels of map source below the top-level parent.

5.  In the **Map sources** related list, select **New**.

    A new Map source \[viz\_map\_source\] record opens, with the Table and Parent fields read-only.

6.  Specify the following information:

<table id="table_bnf_gxf_cyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the map source. Include the level in the names of map source levels. Generally give all map sources in the same hierarchy the same root name. Differentiate them only by level, such as Location mapping \(level 2\) and Location mapping \(level 3\).

</td></tr><tr><td>

Table \(read-only\)

</td><td>

The same table is used throughout a map source hierarchy, and is specified in the top-level map source.

</td></tr><tr><td>

Field

</td><td>

Select a field of location data that is one level more granular than the map you are displaying it on.For example, imagine you are configuring data for a level 1 map source that is displayed on the world map. Because the data for countries are displayed on the world map, select **Location Country**. Similarly, if you are configuring data to display on a map of Germany or the United States, select **Location State / Province**.

**Note:** The city is the most granular location level that you can display when drilling down into a map report. For example: If you want to report on various site locations within a city, and define the bottom-level map source field to include location.name, the map report displays the multiple locations as the corresponding city labels. As a result, reporting on multiple locations which have the same location.city value results in displaying multiple map dots with the same label, but with different aggregated values, and which drill down to different locations.

</td></tr><tr><td>

Level

</td><td>

Select a hierarchy level for this map source. You must select a level that is one level lower than the parent map source's level. You can have a maximum of four levels. Each map source level corresponds to a drill level on the map hierarchy, and these levels much match. Only one map source of the same level can exist in a hierarchy at the same time.

</td></tr><tr><td>

Active

</td><td>

Clear this check box to make this map source unavailable when creating map reports.

</td></tr></tbody>
</table>7.  In the **Data transformation** section, specify the following information:

<table id="table_wxt_3dg_1v"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

How to use data

</td><td>

Select how to use data in this map source. -   **Use data on table**: Use the data in the ServiceNow AI Platform® without transforming it. Select this option when the data already matches the JSON key values that you’re mapping to.
-   **Use mapping**: The most common use case. Transform data so it matches the JSON key values that you’re mapping to. For geographical map sources that use the hc-key geoJSON key, always select this option.

This option can’t be used with data below the state/province level, because **Region and state** is the lowest level mapping.

-   **Use latitude and longitude**: Always select this option for the bottom map level, such as level 3. Ensure that your data has latitude and longitude values.

**Warning:** Because the **Use longitude and latitude** option disables drilling down, select this option only on map source levels that are the bottom level in a hierarchy.

</td></tr><tr><td>

Use these mappings

</td><td>

If you selected **Use mapping**, select a mapping group to use. A mapping group is a collection of key-value pair mappings that transform data. To review the mappings in a mapping group, go to the Locations Mappings \[sys\_report\_map\_source\_mapping\] table.For example, if you’re transforming field value **USA** to hc-key value **us**, select **Country mappings**, which contains the relevant key-value pair mapping.

</td></tr></tbody>
</table>8.  In the **JSON key** section, select a JSON key to connect the map source data to maps.

    Geographical maps typically use hc-key.

    Every geomap has a JSON definition. Select one JSON key-value pair to map the data to. The data to appear on the map must match the JSON key values. So the key that you select determines whether you must transform your data with the settings in the **How to use data** section. All default platform maps and mappings use the [geoJSON](http://geojson.org/) hc-key and ISO 3166 standard values. For custom maps, you can enter a different JSON key.

9.  Select **Update**.


