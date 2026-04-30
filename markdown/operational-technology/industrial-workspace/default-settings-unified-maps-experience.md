---
title: Default settings of the Operational Technology Unified Map experience
description: You can modify the default settings available for the Operational Technology \(OT\) Unified Map experience.
locale: en-US
release: yokohama
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up the Operational Technology Unified Map experience, Configure, Industrial Workspace, Operational Technology]
---

# Default settings of the Operational Technology Unified Map experience

You can modify the default settings available for the Operational Technology \(OT\) Unified Map experience.

With the admin role, you can modify the default settings of the Industrial Workspace Config Identifier available with the OT Unified Map experience. A configuration identifier, or config identifier, is a configuration element within the configuration identifiers framework. A config identifier contains settings and table-driven configurations used in a UX application such as a workspace.

If a property isn't set or if there are no entries in the table-driven configuration, look-up uses the values in the default configuration identifier instead. For more information about the configuration identifiers framework, see [Configuration identifiers framework](https://www.servicenow.com/docs/access?context=configuration-identifiers-framework&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

To access the Industrial Workspace Config Identifier record, navigate to **All**, and in the filter bar, enter `sn_cmdb_ws_config_identifier.list`. Then select **Industrial Workspace Config Identifier**.

The following sections describe the default settings available to modify in the Industrial Workspace Config Identifier.

**Note:** The settings described affect all users. Individual users can’t configure the settings.

**Workspace Config Properties**

By default, the following configuration properties are listed in the `sn_cmdb_ws_config_property.list` and are assigned to the default configuration identifier.

-   unifiedmap.map\_search.max\_nodes
-   unifiedmap.map\_search\_filter.default\_levels
-   unifiedmap.map\_search\_filter.max\_levels
-   unifiedmap.map\_search\_filter.endpoint\_deduplication\_fields

**Node Map Profiles**

You can configure profiles that set default map filters and default map orientation for a class. For example, to show the service-mapping data for the Mapped Application Service class.

These class profiles help in identifying which layers are shown on the Unified Map for a given configuration item \(CI\) node. Class profiles are applied when no filter preset is used with the current map. This application typically occurs when you initially load a map without a filter preset, or when you set the filter preset to the default view.

With class profiles, you can only configure the **Layer** category in the filter panel.

**Node Map References**

Map references enable connections on the map between CIs from two classes that aren't connected by a relationship.

**Node Map Related Items**

You can use the Related Items module in the Unified Map to set the related items categories that appear for CIs, such as active incidents and active problems. When you select the Related Items module, related items are grouped by categories in the contextual side panel.

**Operational life cycle modes**

You can specify the operational states that CIs must have for them to be included in the Unified Maps.

**Table Attributes**

Each class has a unique set of extended properties that appear in the Unified Map Attributes panel for a CI. Many common classes are preconfigured with these properties. You can modify the default settings and globally configure extended properties for additional classes.

**Parent Topic:**[Setting up the Operational Technology Unified Map experience](../task/setting-up-unified-maps-experience.md)

