---
title: Virtual grouping of nodes in a Dependency Views map
description: To reduce the density on a map, Dependency Views automatically groups CIs of a similar CI type from the same level.
locale: en-US
release: zurich
product: Dependency Views
classification: dependency-views
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Virtual grouping of nodes in a Dependency Views map

To reduce the density on a map, Dependency Views automatically groups CIs of a similar CI type from the same level.

A large number of nodes can cause a Dependency Views map to become too dense to be helpful. Therefore, if the number of nodes with a similar CI type from same level, exceeds the value of the **Maximum number of nodes \(of a similar CI type and at the same level\) to display before applying virtual grouping** property, then those nodes are automatically grouped into a virtual group. A single node, the virtual group node is displayed to represent the virtual group, while all actual nodes in the virtual group \(that are of a similar CI type\), are hidden. Virtual group nodes represent CIs of a similar CI type but are not CIs by themselves and cannot have tasks assigned to them. The number of actual collapsed nodes in the virtual group is noted on the virtual group node.

By default, child nodes of a virtual group are not displayed. You can enable the **Show children of virtual groups** property to display child nodes underneath virtual groups.

Virtual grouping is not applied at the level underneath a virtual group even if the criteria for virtual grouping is met \(the number of nodes with a similar CI type from that level exceeds the preconfigured property value\). However, virtual grouping can happen at the following level if that criteria is met. This behavior does not depend on any property settings, and you cannot change it.

Menu options for a virtual group include **Expand** and **Collapse**, which allow you to apply virtual grouping and display only the virtual group node, or to undo the virtual grouping and display all actual nodes.

## Virtual links

A virtual node is connected to other nodes with a virtual link. A virtual link denotes that there such link between at least one CI in the virtual group, to another CI node on the map.

**Note:** Predefined filters do not apply to virtual groups. Therefore a virtual group displays even if it contains CIs that a predefined filter would have excluded. Upon the expansion of a virtual group, predefined filters are applied, and any or all of the CIs that were previously virtually grouped, might no longer display on the map.

Also, when using the node menu option **Load More**, virtual grouping is not applied at the newly loaded level even the criteria for virtual grouping is met.

![An expanded virtual group displays its nodes and its child nodes.](../image/VGCollapsedandExpanded.png "An expanded virtual group")

**Related topics**  


[Properties for Dependency Views](../reference/properties-dependency-views.md)

