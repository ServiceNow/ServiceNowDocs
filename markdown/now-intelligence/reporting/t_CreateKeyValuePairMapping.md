---
title: Create a key-value pair mapping
description: Key-value pair mappings transform data in the ServiceNow platform to a value that can be plotted on a map. Mappings are used during map source configuration when data requires transformation. Each mapping exists in a mapping group.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Map report administration, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a key-value pair mapping

Key-value pair mappings transform data in the ServiceNow platform to a value that can be plotted on a map. Mappings are used during map source configuration when data requires transformation. Each mapping exists in a mapping group.

## Before you begin

Role required: report\_admin or admin.

## About this task

Default system key-value pairs map data to geoJSON hc-key values. All hc-key values follow ISO 3166 standards. Default mappings exist for the most commonly used data values. If your data uses a different value, you must create a key-value pair mapping.

For example, the default mapping for United States of America maps key USA to `ISO` value `us`. If your data has value of United States instead of USA, you must make a new key-value pair to map `United States` to ISO value `us`.

## Procedure

1.  Navigate to the Locations Mappings \[sys\_report\_map\_source\_mappings\] table.

2.  In the **Map Source Mapping** column, select the mapping group to add the mapping to.

    Select the mapping group that corresponds to type of object that you want to create a mapping for. For example, if you are creating a mapping for field value United States, select the **Country mappings** group. Note that the Key and Map values in the row with the mapping aren't taken into account.

    ![Location mappings table with Map Source Mapping column highlighted](../image/select-mapping.png "Select map source mapping")

3.  Select **New**.

4.  Fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Key|The field value to transform. For example, USA.|
    |Value|The value to transform the key to. For example, us. This value is typically an ISO 3166 standard value. Each value can be used only once per map.|
    |Map|The map to associate with this mapping. If you do not fill in this field, this mapping can be used with any map.|

5.  Select **Submit** to save your changes.


## What to do next

Add the mapping to a report source, so it can be used to map data from that source to a map.

**Parent Topic:**[Map report administration](../concept/c_AdministeringMapReports.md)

**Related topics**  


[Map report objects](../concept/c_MapReportObjects.md)

[Automatically generate a map source hierarchy](t_AutoGenerateMapSourceHierarchy.md)

[Customize a map source level](t_CustomizeAMapSourceLevel.md)

[Create a map](t_CreateAMap.md#)

