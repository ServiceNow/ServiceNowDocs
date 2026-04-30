---
title: Configure how to display related items on the map
description: Add related items categories, specify which information should appear on cards on the Unified Map Related items panel, and specify how related items \(events\) appear on the timeline and on badges. These are general settings that only sn\_cmdb\_admin can configure.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure how to display related items on the map

Add related items categories, specify which information should appear on cards on the Unified Map **Related items** panel, and specify how related items \(events\) appear on the timeline and on badges. These are general settings that only sn\_cmdb\_admin can configure.

## Before you begin

Set the application scope in your instance to **CMDB Workspace**.

Role required: sn\_cmdb\_admin

## About this task

These workspace-specific configuration settings affect all users of the CMDB Unified Map page. The settings do not affect other copies of the Unified Map template. Configuration settings that non-admin users can specify are described in [Configure the Related items panel](unified-map-configure-rel-items.md).

Related items are grouped by category in the **Related items** panel. Related items also appear for CI badges on the map and timeline.

The \[sn\_cmdb\_ws\_node\_map\_related\_item\] table contains the settings that determine which related items and associated details appear. By default, common categories of related items, such as active incidents and other events for example, are configured to appear. You add or modify records to globally manage related items on maps.

## Procedure

1.  Navigate to **All** and then, in the search box on the main navigation bar, enter `sn_cmdb_ws_node_map_related_item.list` to open the Node Map Related Item table.

2.  Select an existing record or select **New** and then fill in the form.

<table id="table_yfs_hwf_nxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The category label that appears on the **Related items** panel for a selected CI.

</td></tr><tr><td>

Table

</td><td>

Tables from which records for the category are retrieved.

</td></tr><tr><td>

Order

</td><td>

Order that the category appears within all related items categories.

 The list of related items categories is sorted in ascending order. The category with the smallest order number appears at the top of the list.

</td></tr><tr><td>

Active

</td><td>

Enables the appearance of the related item category.

</td></tr><tr><td>

Reference field

</td><td>

Reference attribute in the specified **Table** that references the CIs for the category. Typically set to **Configuration Item \[cmdb\_ci\]**.

</td></tr></tbody>
</table>3.  Select the Related fields and conditions tab and then fill in the settings.

    | | |
    |---|---|
    |Number field|Numeric attribute from the specified table that uniquely identifies each record in the category. This attribute is used in the record link that appears on each card when drilling down the related item category.|
    |Title field|Attribute from the specified table that appears as the title of each card when drilling down the category in the panel.|
    |Fields|Set of attributes from the specified table that appears on each card when drilling down the related item category. For example, when drilling down alerts, the set of attributes that appears on each alert card.|
    |Sort fields|Order of appearance of the fields specified in the **Fields** setting.|
    |Footer field|Attribute from the specified table that appears at the bottom of individual cards when drilling down the related item category, regardless of the sort order specified in the **Sort fields** setting.|
    |Conditions|Conditions to apply to the specified table that retrieve the set of records for the category.|

4.  Select the Badge and timeline configuration tab and then fill in the settings.

<table id="table_vfs_mbz_byb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Badge and timeline icon

</td><td>

Icon that appears on CI badges and on the timeline for the specified related item.

</td></tr><tr><td>

Badge and timeline highlight field

</td><td>

Highlight configuration for applying colors to timeline and map icons.

</td></tr><tr><td>

Date field

</td><td>

The date field to position the event on the timeline.

</td></tr><tr><td>

End date field

</td><td>

Optional end date field to use for a range on the timeline.

</td></tr></tbody>
</table>5.  Select **Submit** or **Update**.

    The updated settings appear in the appropriate related list on the Configuration identifier form, as described in [Configuring Unified Map — Admin settings](../concept/administer-unified-map.md).


**Parent Topic:**[Configuring Unified Map — Admin settings](../concept/administer-unified-map.md)

**Related topics**  


[View related items for a CI](unified-map-show-related-items.md)

[Viewing related items on the Unified Map timeline](../concept/unified-map-timeline-working-on.md)

