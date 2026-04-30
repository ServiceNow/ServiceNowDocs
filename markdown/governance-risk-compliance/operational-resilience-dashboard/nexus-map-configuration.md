---
title: Nexus map configurations
description: Beginning with Operational Resilience, version 21.1.x, the Nexus map configuration has been introduced. To display a main node in the Operational Resilience Workspace, you must configure the Nexus map. The Node Map configuration UI allows you to visualize related data hierarchically, track issues, and identify areas needing attention for effective resolution or health monitoring.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-11-03"
reading_time_minutes: 3
breadcrumb: [Main node configurations: A component of the Data Relationship Framework, Explore, Operational Resilience, Governance, Risk, and Compliance]
---

# Nexus map configurations

Beginning with Operational Resilience, version 21.1.x, the Nexus map configuration has been introduced. To display a main node in the Operational Resilience Workspace, you must configure the Nexus map. The Node Map configuration UI allows you to visualize related data hierarchically, track issues, and identify areas needing attention for effective resolution or health monitoring.

## Limitations observed before using Nexus map configurations

Before implementing Node map configurations with Operational Resilience, version 21.1.x, visualizing dependencies across multiple stages of the Common Service Data Model \(CSDM\) in various Workspace views was challenging. The data hierarchies, as shown in the following example model, are complex and multidimensional, making it difficult to understand relationships between different data entities:

-   Business Service → Business Service Offering → Business Process → Application → Dependencies
-   Entity → Policy → Control Objective → Control → Control Indicator

List views alone are insufficient for effectively depicting complex relationships, often requiring manual navigation through multiple related lists and records to understand upstream or downstream impacts. Node map configurations offer a more efficient solution, enabling you to visualize these complex relationships easily.

## Benefits of Nexus map configurations

The Node map configurations, which are part of Data Relationships Framework by default, enable you to define relationships between records and visualize them on a node map. This visualization makes it easier to understand upstream and downstream relationships.

The Node map configuration feature offers the following benefits:

-   It enables any consuming application to define relationships between records and visualize related data hierarchically on a node map.
-   It facilitates issue tracking and identification of areas requiring attention for troubleshooting purposes.

## Dependencies for Nexus map configurations

The Node map configurations have the following hard dependencies:

-   Data registry for defining data relationships \(sn\_data\_registry\)
-   Record Related Items Connected \(sn\_rec\_relatedItem\)

The Node map configuration has the following optional dependencies:

-   Providing 360° Relationship Visualization for rendering 360º view and related items
-   Using GRC: Common Workspace Elements for navigating to 360º view and related items

## Record visibility based on user access

Access to records is determined by the read access control lists \(ACLs\) associated with those records. You can only view records that you have access to. Nodes and their underlying children that you don’t have access to, aren’t displayed in the map.

This functionality verifies that sensitive information is protected and you can only see data that you’re authorized to access.

For details on Nexus map configurations, including Node and Edge configurations, refer to the "Nexus map configurations related list" in [Main node configurations: A component of the Data Relationships Framework](main-node-relationship-fw.md).

-   **[Node and edge configurations and property setting from the UI](configuration-for-node-map.md)**  
To access the Node map configuration from the Operational Resilience Workspace, BCM administrators must set up the Main node configurations. Once the Main node configuration table is set up, it enables you to create configurations for entities such as services, business services, offerings, business processes, and application services. You can update the properties, node, and edge configuration details.

**Parent Topic:**[Main node configurations: A component of the Data Relationships Framework](main-node-relationship-fw.md)

