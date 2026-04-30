---
title: Configure display of connections to a referenced class
description: Configure how to display connections to a referenced class and from a referencing class on Unified Map. A reference connects two CIs from differing classes that aren't connected by a relationship. These are general settings that only sn\_cmdb\_admin can configure.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure display of connections to a referenced class

Configure how to display connections to a referenced class and from a referencing class on Unified Map. A reference connects two CIs from differing classes that aren't connected by a relationship. These are general settings that only sn\_cmdb\_admin can configure.

## Before you begin

Set the application scope in your instance to **CMDB Workspace**.

Role required: sn\_cmdb\_admin

## About this task

These workspace-specific configuration settings affect all users of the CMDB Unified Map page. The settings do not affect other copies of the Unified Map template. Non-admin users can customize some aspects of their personal experience with Unified Map, but can't configure instance-wide workspace-specific settings.

References connect CIs from two classes that don't have a direct relationship connection between them. On the map, any two CIs from the referenced class and from the referencing class appear connected by a dotted line. The relationship type is **Reference**. There are several preconfigured map references that you can modify, and you can also add map references.

For example, you want the map to display references to records in the File System table for Windows Server CI records. In that case, Server ABC \(referencing CI\) shows connections to the C:\\ and D:\\ file systems \(referenced CIs\).

## Procedure

1.  Navigate to **All** and then, in the filter box on the main navigation bar, enter `sn_cmdb_ws_node_map_reference.list`.

2.  On the Node Map References table, select an existing record or select **New** and then fill in the form.

    |Field|Description|
    |-----|-----------|
    |CI class|The referencing class that this configuration applies to.|
    |Referenced CI class|Class that the specified **Reference field** references.|
    |Reference field|Attribute in the specified **CI class** that contains the reference.|
    |Show Reverse|Creates a map reference for the reverse reference between the specified **CI class** and **Referenced CI class**.|
    |Active|Enables the configuration so that the connection appears on maps — the map displays referenced CIs.|

3.  Select **Submit** or **Update**.

    The updated settings appear in the appropriate related list on the Configuration identifier form, as described in [Configuring Unified Map — Admin settings](../concept/administer-unified-map.md).


**Parent Topic:**[Configuring Unified Map — Admin settings](../concept/administer-unified-map.md)

