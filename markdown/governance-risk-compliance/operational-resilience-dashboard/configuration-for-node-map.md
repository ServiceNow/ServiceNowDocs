---
title: Node and edge configurations and property setting from the UI
description: To access the Node map configuration from the Operational Resilience Workspace, BCM administrators must set up the Main node configurations. Once the Main node configuration table is set up, it enables you to create configurations for entities such as services, business services, offerings, business processes, and application services. You can update the properties, node, and edge configuration details.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-11-03"
reading_time_minutes: 2
breadcrumb: [Nexus map configurations, Main node configurations: A component of the Data Relationship Framework, Explore, Operational Resilience, Governance, Risk, and Compliance]
---

# Node and edge configurations and property setting from the UI

To access the Node map configuration from the Operational Resilience Workspace, BCM administrators must set up the Main node configurations. Once the Main node configuration table is set up, it enables you to create configurations for entities such as services, business services, offerings, business processes, and application services. You can update the properties, node, and edge configuration details.

## Main node configuration properties tab in the UI

The main node configuration comprises several key properties:

-   Maximum number of nodes and levels
-   An order field that auto-increments by 10 \(You can update the order field manually.\)
-   A direction property defining relationships between configuration items and entities

You can update these property settings from the UI directly. For more information on setting up the Main node configurations in your instance, see [Configure the Main node configurations](../task/set-up-main-node.md).

## Nexus map configuration related list in the Main node configuration

As of Operational Resilience, version 21.1.x, the Nexus map configuration related list is available within the Main node configuration. This enhancement enables you to create multiple configurations for a single main node. You can designate a default configuration for a main node, which is used when loading the node map. The Nexus map configuration consists of two distinct aspects: node configuration and edge configuration.

## Node and edge configurations

The node configuration defines the visual representation of nodes, including their icon, tooltip, primary label, and secondary label. In contrast, the edge configuration determines the appearance of the connections between nodes, such as line type, color, label, and tooltip.

To access the entity hierarchy graphically, select the **Resilience Map** button on an entity's **Overview** tab in the Operational Resilience Workspace list view. The node map illustrates the entity hierarchy based on upstream and downstream relationships.

## User roles and UI display

The Nexus map feature is accessible to multiple user roles, although its configuration settings are read-only. The configuration for Nexus Map is managed through the Main node configuration, with related lists for the node relationship and edge configurations. You can customize properties such as maximum number of nodes, maximum number of children, and edge properties. Based on your configuration settings, the resulting node map is displayed in the UI.

**Parent Topic:**[Nexus map configurations](nexus-map-configuration.md)

