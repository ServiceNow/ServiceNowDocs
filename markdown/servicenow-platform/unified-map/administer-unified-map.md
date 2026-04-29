---
title: Configuring Unified Map — admin settings
description: Administrators can configure general Unified Map settings to control the initial content and appearance of maps for all users in a workspace.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring Unified Map — admin settings

Administrators can configure general Unified Map settings to control the initial content and appearance of maps for all users in a workspace.

## Activating Unified Map

To activate Unified Map, set up the CMDB Workspace ServiceNow Store app and then enable the **sn\_sm\_scoped\_app.sa.unified\_map.enabled** system property.

For more information, see [Set up CMDB Workspace](setup-cmdb-workspace.md).

## Unified Map settings that admins can configure

These workspace-specific configuration settings affect all users of the CMDB Unified Map page. The settings do not affect other copies of the Unified Map template.

-   [Create or manage a shared preset](../task/unified-map-manage-shared-preset.md)
-   [Configure how many nodes can appear on a map](../task/unified-map-cfg-max-nodes-on-maps.md)
-   [Configure the default or maximum number of levels on maps](../task/unified-map-cfg-levels-on-maps.md)
-   [Configure endpoint de-duplication on maps](../task/unified-map-cfg-endpnt-deduplicate.md)
-   [Configure CIs to appear based on life cycle stage value](../task/unified-map-confg-operational-state.md)
-   [Configure how to display related items on the map](../task/unified-map-config-related-items.md)
-   [Configure which attributes to display in the Attributes panel](../task/unified-map-config-extended-prop.md)
-   [Configure display of connections to a referenced class](../task/unified-map-config-map-references.md)
-   [Create a class profile of visible layers for classes](../task/unified-map-config-class-profile.md)
-   [Create or manage a shared preset](../task/unified-map-manage-shared-preset.md)

## How configuration settings for Unified Map are stored

See [How configuration settings for Unified Map are stored](unified-map-config-settings-viewing.md).

## Unified Map settings that non-admin users can configure

Non-admin users can customize some aspects of their personal experience with Unified Map, but can't configure instance-wide workspace-specific settings. Non-admin users can control which elements appear on the map, isolate and analyze relationships between CIs, and simplify the map to isolate issues.

For more information, see [Controlling Unified Map contents and appearance](../reference/unified-map-appearance.md).

-   **[Create or manage a shared preset](../task/unified-map-manage-shared-preset.md)**  
Admins can save a set of Unified Map map filter settings \(layer, CI class, relationship type, and other CI attribute settings\) as a shared preset that any user can apply to their map view.
-   **[Configure how many nodes can appear on a map](../task/unified-map-cfg-max-nodes-on-maps.md)**  
Configure the maximum number of nodes that can be loaded when a map in this workspace opens. These are general settings that only sn\_cmdb\_admin can configure.
-   **[Configure the default or maximum number of levels on maps](../task/unified-map-cfg-levels-on-maps.md)**  
Configure the default or maximum number of levels on maps. These are general settings that only sn\_cmdb\_admin can configure.
-   **[Configure endpoint de-duplication on maps](../task/unified-map-cfg-endpnt-deduplicate.md)**  
Configure how duplicate edges are displayed on maps. These are general settings that only sn\_cmdb\_admin can configure.
-   **[Configure CIs to appear based on life cycle stage value](../task/unified-map-confg-operational-state.md)**  
By default, only CIs for which **Life cycle stage** is **Operational** or empty appear on maps. You can configure the map to display CIs with other **Life cycle stage** values. These are general settings that only sn\_cmdb\_admin can configure.
-   **[Configure how to display related items on the map](../task/unified-map-config-related-items.md)**  
Add related items categories, specify which information should appear on cards on the Unified Map **Related items** panel, and specify how related items \(events\) appear on the timeline and on badges. These are general settings that only sn\_cmdb\_admin can configure.
-   **[Configure which attributes to display in the Attributes panel](../task/unified-map-config-extended-prop.md)**  
Each class has a unique set of extended attributes that appear in the bottom section of the **Attributes** panel for a CI. For any class, you can specify which extended attributes should be displayed. These are general settings that only sn\_cmdb\_admin can configure.
-   **[Configure display of connections to a referenced class](../task/unified-map-config-map-references.md)**  
Configure how to display connections to a referenced class and from a referencing class on Unified Map. A reference connects two CIs from differing classes that aren't connected by a relationship. These are general settings that only sn\_cmdb\_admin can configure.
-   **[Create a class profile of visible layers for classes](../task/unified-map-config-class-profile.md)**  
Configure a class profile that specifies which layers should appear for a particular class: application, service instance, business, or infrastructure. For example, you can configure that the mapped application service \(service instance\) \[cmdb\_ci\_service\_discovered\] class should display only Service Mapping data and not infrastructure elements.
-   **[How configuration settings for Unified Map are stored](unified-map-config-settings-viewing.md)**  
General configuration settings that control Unified Map are collected in a configuration identifier. A configuration identifier is a set of properties and table-driven configurations that specify the appearance and content of an instance of a UX application. The **CMDB Workspace** UX application contains Unified Map.

**Parent Topic:**[Unified Map](../reference/unified-map-landing-page.md)

**Related topics**  


[Configuration identifiers framework](configuration-identifiers-framework.md)

[How configuration settings for Unified Map are stored](unified-map-config-settings-viewing.md)

