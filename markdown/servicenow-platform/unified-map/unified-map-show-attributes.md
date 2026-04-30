---
title: View the attributes of a CI or a relationship
description: Open the Attributes panel in Unified Map to view attributes like location and life cycle stage for a CI or a relationship.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View the attributes of a CI or a relationship

Open the **Attributes** panel in Unified Map to view attributes like location and life cycle stage for a CI or a relationship.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational service instances: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational service instances: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

When you select a group CI such as a service instanceor a dynamic CI group as the home node, the **Attributes** panel shows the attributes of the group CI itself and a card for each CI and relationship member of the group. When you open a map for a service instance CI, a badge on group CIs shows the number of members. Select a badge to expand or collapse the group.

## Procedure

1.  While working in a map, select a CI or a relationship on the map and then select the Attributes icon ![](../image/icon-um-attributes-panel.png).

    ![Attributes of the selected CI.](../image/um-attributes-panel.png)

    The **Attributes** panel shows the following details:

    -   For a non-group CI: The top section displays base properties — common key attributes, such as **Class** and **Discovery source** that appear for CIs of any class \(other than service instance CIs\). You cannot change the group of properties that appear in this section.
    -   The bottom section displays extended properties — attributes that uniquely extend the class of a CI in the CMDB hierarchy. You can specify the properties that should appear in this section. For more information, see [Configure which attributes to display in the Attributes panel](unified-map-config-extended-prop.md).
    -   For a group CI: The top card shows attributes of the group CI. The cards in the Configuration items section display attributes for each of the group member CIs.
    -   For a single relationship: A card with the attributes for the selected relationship.
    -   For a multi-relationship badge: A card for each of the relationships in the relationship set that shows the attributes for the relationship. The number of cards is equal to the number on the relationship badge, which is a count of the different types of relationships between the two CIs in that direction. Relationship connections are based on records in the CI Relationship \[cmdb\_rel\_ci\] table.

## What to do next

In a CI card on the **Service instances** panel, select the **Actions** menu and then select any of the following options:

-   Select **View CI details** to open the CI form for the CI.
-   Select **Open in new map** to open an additional map with the current CI set as the home node.
-   Select **Set CI as home** to set the selected CI as the home node for the map.

Select a mapped service instance \(formerly application service\) CI \[cmdb\_ci\_service\_discovered\] on the map to display its entry points on the **Attributes** panel.

