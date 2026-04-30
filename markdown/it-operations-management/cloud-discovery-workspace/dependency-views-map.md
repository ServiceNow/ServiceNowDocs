---
title: Dependency Views map
description: ServiceNow The Dependency Views map shows an overall top-down Kubernetes perspective, starting from a top-level cluster to the container and within the container.
locale: en-US
release: xanadu
product: Cloud Discovery Workspace
classification: cloud-discovery-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cloud Discovery Workspace, ITOM Visibility, IT Operations Management]
---

# Dependency Views map

ServiceNow® The Dependency Views map shows an overall top-down Kubernetes perspective, starting from a top-level cluster to the container and within the container.

A Dependency Views map has one starting point, called the root CI or root node of the map. The root CI is surrounded by a darker frame that repaints itself with a pulsing effect drawing the attention to the root CI. The maps can show both upstream and downstream dependencies for the root CI. By default the Dependency Views map displays three levels, both upstream and downstream relationships. Administrators can configure the number of levels displayed. The map collapses and expands clusters to make them easier to view. By default, clusters are collapsed.

The Dependency Views module is active in all instances, and includes demo data.

![CIs and connections on a Dependency Views map.](../image/DependencyView.png "Dependency Views sample map")

In a Dependency Views map, map indicators indicate if a CI has any active, pending issues. You can investigate the tasks that are connected to a CI to get more details. When you return to the map from another form, the system restores the last map viewed, using the default filter and layout settings.

Many of the relationships in the map are created through the discovery process. You can also create, define, and delete CI relationships in the map. You can display the map from different perspectives and open specific records that relate to configuration items. The system refreshes the map automatically to reflect changes to the CMDB.

**Note:** CIs not extended from the Configuration Item \[cmdb\_ci\] table, aren’t displayed in Dependency Views maps and in CI relation formatters.

## Roles

Users with the itil and ecmdb\_admin roles can view maps and perform all actions in the map. Actions include access to the map views and saved filters, both from the lists in the map and from the **Saved Filters** module.

