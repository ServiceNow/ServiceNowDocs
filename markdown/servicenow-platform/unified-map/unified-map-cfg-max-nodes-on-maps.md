---
title: Configure how many nodes can appear on a map
description: Configure the maximum number of nodes that can be loaded when a map in this workspace opens. These are general settings that only sn\_cmdb\_admin can configure.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure how many nodes can appear on a map

Configure the maximum number of nodes that can be loaded when a map in this workspace opens. These are general settings that only sn\_cmdb\_admin can configure.

## Before you begin

Set the application scope in your instance to **CMDB Workspace**.

Role required: sn\_cmdb\_admin

## About this task

Admins can set the maximum node count using the **unifiedmap.map\_search.max\_nodes** property in the workspace-specific \[sn\_cmdb\_ws\_config\_property\] table.

These workspace-specific configuration settings affect all users of the CMDB Unified Map page. The settings do not affect other copies of the Unified Map template.

## Procedure

1.  Navigate to **All** and then, in the filter box in the main navigation bar, enter `sn_cmdb_ws_config_property.list`.

2.  Select the **unifiedmap.map\_search.max\_nodes** property.

3.  Select **New** or select the configuration identifier to update and then fill in the form.

<table id="table_wjp_scm_nxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Config identifier

</td><td>

Unique name of the configuration identifier that specifies the settings for the current workspace.

 **Note:** The base system includes a configuration identifier named **Default** that specifies the default settings for Unified Map.

</td></tr><tr><td>

Name

</td><td>

The name of the property that you're updating: unifiedmap.map\_search.max\_nodes.

</td></tr><tr><td>

Value

</td><td>

Maximum count of nodes that are loaded when a map in this workspace opens.

</td></tr><tr><td>

UX application

</td><td>

The top-level **UX Application ID** to which this configuration applies. This is the application ID of your workspace. This value is referenced from the record associated with the **Config identifier** setting.

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.

    The updated settings appear in the appropriate related list on the Configuration identifier form, as described in [Configuring Unified Map — Admin settings](../concept/administer-unified-map.md).


**Parent Topic:**[Configuring Unified Map — Admin settings](../concept/administer-unified-map.md)

