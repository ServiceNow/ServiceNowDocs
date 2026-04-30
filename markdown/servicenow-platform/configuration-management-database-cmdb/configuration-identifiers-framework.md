---
title: Configuration identifiers framework
description: Configuration identifiers provide a framework that lets you customize some behaviors of a CMDB Workspace feature, enabling different settings for that feature, on different workspaces. Most importantly, you can use this customization framework when integrating a CMDB Workspace feature into another workspace.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuration identifiers framework

Configuration identifiers provide a framework that lets you customize some behaviors of a CMDB Workspace feature, enabling different settings for that feature, on different workspaces. Most importantly, you can use this customization framework when integrating a CMDB Workspace feature into another workspace.

## Configuration identifier

A configuration identifier \(also referred to as config identifier\) is a configuration element within the configuration identifiers framework. A config identifier contains custom settings for a CMDB Workspace feature, that is applicable to a specific workspace. A config identifier contains settings and table-driven configurations used in a UX application such as a workspace. Using config identifiers lets you for example, integrate CMDB Workspace Unified Map into another workspace, with the integrated Unified Map being customized for the workspace. Config identifiers are stored in the Config identifiers \[sn\_cmdb\_ws\_config\_identifier\] table.

A config Identifier acts as the parent record for a set of configurations that are specific to a workspace and therefore overrides default behavior only for that workspace.

## Default config identifier

Initially, the Config identifiers \[sn\_cmdb\_ws\_config\_identifier\] table in CMDB Workspace, contains a single config identifier named ‘Default’ and which is workspace-agnostic. This Default config identifier has its **Default** column set to **Yes**, a setting that can't be modified. Only a single config identifier can be set to **Yes**, therefore, any additional config identifiers that you create are set to **No**.

The default config identifier contains default settings for CMDB Workspace features. Any subsequent Config Identifier that you configure, is set for a specific workspace. When integrating a CMDB Workspace feature into another workspace and there are no entries in the table-driven configuration for that feature, look-up uses the settings in the default configuration identifier.

## Key roles

The following roles are needed in order to use the configuration identifiers framework:

-   sn\_cmdb\_ws.config\_editor: Can modify child config tables, such as sn\_cmdb\_ws\_config\_property.
-   sn\_cmdb\_ws.config\_admin: Can modify both sn\_cmdb\_ws\_config\_identifier and child config tables.
-   sn\_cmdb\_admin: Role required to modify default config records under the default identifier or the default identifier itself.

For more information about these roles, see [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md).

## Examples of CMDB Workspace features using the configuration identifiers framework for feature settings

-   Unified Map:
    -   [Configure how many nodes can appear on a map](../task/unified-map-cfg-max-nodes-on-maps.md)
    -   [Configure the default or maximum number of levels on maps](../task/unified-map-cfg-levels-on-maps.md)
    -   [Configure endpoint de-duplication on maps](../task/unified-map-cfg-endpnt-deduplicate.md)
    -   [Configure which attributes to display in the Attributes panel](../task/unified-map-config-extended-prop.md)
    -   [Create a class profile of visible layers for classes](../task/unified-map-config-class-profile.md)
    -   [Configure CIs to appear based on life cycle stage value](../task/unified-map-confg-operational-state.md)
-   Create CI:
    -   [Request additional attributes for new CIs](../task/additional-att-create-ci-workspace.md#)
    -   [Limit the class list for new CIs created in a workspace](../task/limit-class-create-ci-workspace.md)

**Parent Topic:**[Exploring CMDB Workspace](exploring-cmdb-workspace.md)

