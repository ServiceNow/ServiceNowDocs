---
title: Automatically generate a map source hierarchy
description: A map source hierarchy is a data source that is used to create a map report. Except for the top-level wrapper, each map source level in the hierarchy defines the data for one map drill level.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Map report administration, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Automatically generate a map source hierarchy

A map source hierarchy is a data source that is used to create a map report. Except for the top-level wrapper, each map source level in the hierarchy defines the data for one map drill level.

## Before you begin

Role required: report\_admin or admin

## About this task

**Note:** A set of predefined map sources and maps are available by default. Use these predefined objects whenever possible. If you need a map source that does not exist, generate it automatically using **Generate map source levels** link on the map source form, then customize it.You can automatically generate map source levels only for map sources that reference the location table. These map sources have a field that ends in `.location`.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Map Sources**.

2.  Click **New**.

3.  Fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a descriptive name. For example, Incident by location. Users select the map source by this name in the **Map data** field when they create a map report.|
    |Table|Select the table that contains the field that you want to map. All map source levels in the hierarchy use this table.|
    |Field|Select the field with the data that you want to display on the map report. This field must reference the location table. For example, **incident.caller.location** or **incident.location**. You can dot walk to this field.|
    |Active|Select this check box to make the map source available when creating map reports.|

4.  Right-click the form header and select **Save**.

5.  Click **Generate map source levels**.

    Three map source levels are created. Only the level 1 map source is visible in the **Map Sources** related list.

    **Note:** A map source can have up to four levels, but only three are automatically generated. If the map hierarchy you are using requires an extra drill level, you can create a fourth level map source.


## What to do next

The map source is ready to use in a map report.

**Parent Topic:**[Map report administration](../concept/c_AdministeringMapReports.md)

**Related topics**  


[Map report objects](../concept/c_MapReportObjects.md)

[Customize a map source level](t_CustomizeAMapSourceLevel.md)

[Create a key-value pair mapping](t_CreateKeyValuePairMapping.md)

[Create a map](t_CreateAMap.md#)

