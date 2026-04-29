---
title: Create a map
description: Create a map that can be used in a map hierarchy.You can change the map that appears by default in the Set map field when you create a map report.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Map report administration, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a map

Create a map that can be used in a map hierarchy.

## Before you begin

Role required: report\_admin or admin.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Maps**, and click **New**.

2.  Fill in the following fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Key|Specify a unique key that links this map to other maps. For default maps, the key is the hc-key value. The key must be included in the geoJSON of the parent map.|
    |Name|Enter a name for the map.|
    |Level|Specify the level for this map in the map hierarchy.|
    |JSON definition|Define the geoJSON for the map. You can [download predefined maps from Highcharts](http://code.highcharts.com/mapdata/).|
    |Parent|Select a parent map for this map. The parent-child relationships define drill levels in a map hierarchy.|
    |Active|Clear this check box to make the map unavailable when creating map reports.|
    |Geographical map|If your map is not geographical, clear this check box. For example, clear this check box for a floor map.|

3.  Right-click the form header and select **Save**.

4.  To add conditions that filter the data in the map:

    1.  Click **New** in the **Map conditions** related list.

    2.  Fill in these fields.

        |Field|Description|
        |-----|-----------|
        |Active|Select this check box to apply this condition.|
        |Table|Specify the table that these conditions apply to. Conditions cannot be shared across tables.|
        |Map source|Select the map source that the condition applies to.|
        |Conditions|Add filter conditions to apply to this map.|

    3.  Click **Submit**.

5.  In the **Report Maps** related list, create a child map to extend the map hierarchy.

6.  Click **Update** to save the map.


**Parent Topic:**[Map report administration](../concept/c_AdministeringMapReports.md)

**Related topics**  


[Map report objects](../concept/c_MapReportObjects.md)

[Automatically generate a map source hierarchy](t_AutoGenerateMapSourceHierarchy.md)

[Customize a map source level](t_CustomizeAMapSourceLevel.md)

[Create a key-value pair mapping](t_CreateKeyValuePairMapping.md)

## Set the default map for map reports

You can change the map that appears by default in the **Set map** field when you create a map report.

### Before you begin

Role required: admin or report\_admin.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Properties**.

2.  In the **Set the default map for reports of type 'Map'** field, type the key of the map that you want to set as default.

    You can find a list of maps under **Reports** &gt; **Administration** &gt; **Maps**.

3.  Click **Save**.


