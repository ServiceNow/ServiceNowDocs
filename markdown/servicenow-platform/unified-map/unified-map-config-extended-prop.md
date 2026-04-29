---
title: Configure which attributes to display in the Attributes panel
description: Each class has a unique set of extended attributes that appear in the bottom section of the Attributes panel for a CI. For any class, you can specify which extended attributes should be displayed. These are general settings that only sn\_cmdb\_admin can configure.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure which attributes to display in the Attributes panel

Each class has a unique set of extended attributes that appear in the bottom section of the **Attributes** panel for a CI. For any class, you can specify which extended attributes should be displayed. These are general settings that only sn\_cmdb\_admin can configure.

## Before you begin

Set the application scope in your instance to **CMDB Workspace**.

Role required: sn\_cmdb\_admin

## About this task

In the base system, extended attributes are preconfigured for many common classes. You can modify the default settings and configure settings for additional classes. This example shows where base attributes \(A\) and extended attributes \(B\) appear in the Attributes panel. For more information on the Attributes panel, see [View the attributes of a CI or a relationship](unified-map-show-attributes.md)

![Attributes of the selected CI.](../image/um-attributes-panel-annotated.png)

These workspace-specific configuration settings affect all users of the CMDB Unified Map page. The settings do not affect other copies of the Unified Map template. Non-admin users can customize some aspects of their personal experience with Unified Map, but can't configure instance-wide workspace-specific settings.

## Procedure

1.  Navigate to **All** and then, in the search box on the main navigation bar, enter `sn_cmdb_ws_node_map_table_attributes.list`.

2.  In the Table Attributes table, select the configuration identifier to update or select **New** and then fill in the form:

<table id="table_xlw_ndb_cyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Config identifier

</td><td>

Unique name of the configuration identifier that specifies the settings for the current workspace.

 **Note:** The base system includes a configuration identifier named **Default** that specifies the default settings for Unified Map.

</td></tr><tr><td>

CMDB Class Name

</td><td>

The class that this configuration applies to.

</td></tr><tr><td>

Display attributes

</td><td>

List of attributes that appear as extended attributes on the **Attributes** panel for CIs in the class that is specified by **CMDB Class Name**.

 You can select from attributes for the class. Unlock the field to add attributes to the **Selected** list.

</td></tr><tr><td>

UX application

</td><td>

The top-level **UX Application ID** to which this configuration applies. This is the application ID of your workspace. This value is referenced from the record associated with the **Config identifier** setting.

</td></tr><tr><td>

Active

</td><td>

Option to set the profile as available for use.

</td></tr><tr><td>

Follow hierarchy

</td><td>

If selected, use the following process to determine which attributes to display.

1.  Start with the attributes specified in **Display attributes**.
2.  Move up the class hierarchy and add each parent's display attributes until encountering a parent where **Follow hierarchy** is deselected.
3.  Add that parent's display attributes and then stop collecting display attributes.
 For nodes that have highlight colors defined: If a display attribute value appears more than once, use the highlight color for the least specific CMDB layer.

 The setting provides the following options:

 -   **Follow hierarchy** selected: A derived CI class uses its own display attributes and inherits display attributes from parents.
-   **Follow hierarchy** not selected: A derived CI class displays only attributes that are specified in its **Display attributes** setting.


</td></tr></tbody>
</table>3.  Select **Submit** or **Update**.

    The updated settings appear in the appropriate related list on the Configuration identifier form, as described in [Configuring Unified Map — admin settings](../concept/administer-unified-map.md).


**Parent Topic:**[Configuring Unified Map — admin settings](../concept/administer-unified-map.md)

**Related topics**  


[View the attributes of a CI or a relationship](unified-map-show-attributes.md)

