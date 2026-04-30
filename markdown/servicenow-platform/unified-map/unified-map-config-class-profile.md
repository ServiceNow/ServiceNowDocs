---
title: Create a class profile of visible layers for classes
description: Configure a class profile that specifies which layers should appear for a particular class: application, service instance, business, or infrastructure. For example, you can configure that the mapped application service \(service instance\) \[cmdb\_ci\_service\_discovered\] class should display only Service Mapping data and not infrastructure elements.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a class profile of visible layers for classes

Configure a class profile that specifies which layers should appear for a particular class: application, service instance, business, or infrastructure. For example, you can configure that the mapped application service \(service instance\) \[cmdb\_ci\_service\_discovered\] class should display only Service Mapping data and not infrastructure elements.

## Before you begin

Set the application scope in your instance to **CMDB Workspace**.

Role required: sn\_cmdb\_admin

## About this task

These workspace-specific configuration settings affect all users of the CMDB Unified Map page. The settings do not affect other copies of the Unified Map template. Non-admin users can customize some aspects of their personal experience with Unified Map, but can't configure instance-wide workspace-specific settings.

Class profiles let you configure the **Layers** filter. Several common classes such as the mapped application service \(service instance\) \[cmdb\_ci\_service\_discovered\] class are preconfigured with class profiles.

Class profiles are applied when no filter preset is used for the current map. This typically happens when you load a map without a filter preset or when you set the filter preset to **Default view**.

## Procedure

1.  Navigate to **All** and then, in the search box on the main navigation bar, enter `sn_cmdb_ws_node_map_profiles.list`.

    The Node Map Profiles table lists all classes for which the **Layers** property is set.

2.  Select an existing record or select **New** and then fill in the form.

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

Layers

</td><td>

**Layers** value to apply when the map opens with a home node that is in the class specified by the **CMDB CI class** setting.

-   Application,
-   Service instance \(formerly application service\)
-   Business
-   Infrastructure
 On the map display, in the **Layers** category, the listed filter values are selected and values that are not in the list are deselected.

</td></tr><tr><td>

CMDB CI class

</td><td>

Class of CI that this profile applies to. Whenever a map opens with a home node of the specified class, the **Layers** values are applied.

</td></tr><tr><td>

Orientation

</td><td>

-   Vertical layout: Displays nodes in a vertical tree pattern: upstream relationships top and downstream bottom. This is the default layout for displaying mapped application services and service instances. In the toolbox, select the Vertical layout icon ![](../image/icon-um-vertical-layout.png).
-   Force layout: Displays nodes in a clustered arrangement around the home node, regardless of upstream or downstream relationships. In the toolbox, select the Force layout icon ![](../image/icon-um-force-layout.png).


</td></tr><tr><td>

UX application

</td><td>

The top-level **UX Application ID** to which this configuration applies. This is the application ID of your workspace. This value is referenced from the record associated with the **Config identifier** setting.

</td></tr><tr><td>

Active

</td><td>

Option to set the profile as available for use.

</td></tr></tbody>
</table>3.  Select **Submit** or **Update**.

    The updated settings appear in the appropriate related list on the Configuration identifier form, as described in [Configuring Unified Map — Admin settings](../concept/administer-unified-map.md).


**Parent Topic:**[Configuring Unified Map — Admin settings](../concept/administer-unified-map.md)

**Related topics**  


[Create or manage a user preset](unified-map-manage-preset-filter.md)

