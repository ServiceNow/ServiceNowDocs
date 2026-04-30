---
title: Dependency Views map
description: ServiceNow Dependency Views maps graphically display CIs that support application or business services and the relationships between the CIs.
locale: en-US
release: zurich
product: Dependency Views
classification: dependency-views
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Dependency Views map

ServiceNow® Dependency Views maps graphically display CIs that support application or business services and the relationships between the CIs.

The [CMDB Workspace](../../configuration-management/concept/cmdb-workspace.md) and [Service Graph Workspace](../../configuration-management/concept/sg-workspace.md) store apps provide the [Unified Map](../../configuration-management/concept/cmdb-workspace-unified-map.md) feature as an alternative to using Dependency Views. Unified Map combines the capabilities of Dependency Views and [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) into a single map experience.

A ServiceNow service \(application service or business service\) is work or goods that are supported by an IT infrastructure. For example, delivering email service to an employee can require services such as email servers, web servers, and the work to configure the user's account.

A Dependency Views map has one starting point, called the root CI or root node of the map. The root CI is surrounded by a darker frame that repaints itself with a pulsing effect drawing the attention to the root CI. The maps can show both upstream and downstream dependencies for the root CI. By default the Dependency Views map displays 3 levels, both upstream and downstream relationships. Administrators can configure the number of levels displayed. The map collapses and expands clusters to make them easier to view. By default, clusters are collapsed.

In a Dependency Views map, map indicators indicate if a CI has any active, pending issues. You can investigate the tasks that are connected to a CI to get more details. When you return to the map from another form, the system restores the last map viewed, using the default filter and layout settings. When you click the icon \(![Open Dependency Views map for the CI.](../image/IconBSMMap.png)\) on a CI record or on a task record that identifies a CI, the map opens.

Many of the relationships in map are created through the discovery process. You can also create, define, and delete CI relationships in the map. You can display the map from different perspectives and open specific records that relate to configuration items. The system refreshes the map automatically to reflect changes to the CMDB.

**Note:** CIs not extended from the Configuration Item \[cmdb\_ci\] table, are not displayed in Dependency Views maps and in CI relation formatters.

The Dependency Views module is active in all instances, and includes demo data.

![CIs and connections on a Dependency Views map.](../image/DependencyView.png "Dependency Views sample map")

When you click the map icon \[![Display Dependency Views map for a CI.](../image/IconBSMMap.png)\] on a CI record or on a task record that identify a CI, a map opens.

## Roles

Users with the itil and ecmdb\_admin roles can view maps and perform all actions in the map. Actions include access to the map views and saved filters, both from the lists in the map and from the **Saved Filters** module.

