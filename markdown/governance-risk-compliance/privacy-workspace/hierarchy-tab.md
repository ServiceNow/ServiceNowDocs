---
title: Hierarchy tab
description: Use the Hierarchy tab to connect your processing activity to applications, vendors, companies, entities, business processes, and other activities. The Hierarchy tab builds a clear picture of how data moves through your organization.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Processing activities, Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Hierarchy tab

Use the Hierarchy tab to connect your processing activity to applications, vendors, companies, entities, business processes, and other activities. The Hierarchy tab builds a clear picture of how data moves through your organization.

## When the Hierarchy tab is available

The Hierarchy tab is not visible when the processing activity is in New state. You must move the processing activity to Discover state before the tab appears. When a processing activity is first moved to Discover state, the Hierarchy tab appears with no data. No relationships exist until you add them.

You can also collect hierarchy information from business users by adding this section as part of an assessment. The hierarchy information is added to the processing activity after the assessment is complete.

## Key concepts

-   **Primary record**

    The processing activity in the context of which you're creating or viewing the relationship. The primary record is always the processing activity you currently have open. When you add a relationship, the Primary Record field is pre-filled with this processing activity and cannot be changed.

-   **Primary node**

    The node for which you're creating the relationship. When only one node has been added to the hierarchy, the primary node is the same as the primary record. Once more nodes are added, the primary node can be any node that has been linked with the processing activity.

-   **Related node**

    The node connected to the primary node by a relationship. Depending on the relationship type selected, the related node can be the source of data flowing into the primary node or the destination of data flowing out of it.

-   **Relationship type**

    Defines how the primary node is connected to the related node. Each relationship type includes a description that explains how the two nodes are related and the direction of data flow between them.

-   **Related node type**

    The type of entity you're connecting as a related node. Related nodes can be processing activities, entities, business processes, business applications, vendors, or companies. Additional record types can be configured based on your organization's needs.


## View lineage map

The Lineage map button in the Hierarchy tab displays a graphical view of all the nodes and relationships connected to the current processing activity. You can use the lineage map to visualize data flows, navigate between connected nodes, and edit or delete relationships.

The lineage map not only displays the nodes directly linked to the current processing activity but also the nodes connected to those nodes. You can trace the entire chain of data transfer across all levels from a single view.

## Part of processing activity

The Part of Processing Activity filter helps you distinguish between the applications, vendors, business processes, companies, entities, and processing activities that are part of the specific processing activity versus those that are linked to it, but not part of it.

Consider the Talent Screening processing activity, which includes SHL, HireVue, and Tableau. While Tableau and HireVue are part of Talent Screening, it is also used in other activities such as Interview Planning, since its data feeds into that process.

Enabling this filter scopes the lineage map strictly to the nodes that belong to Talent Screening. To explore the broader data landscape, toggle the filter off to access the global map, where you can see how HireVue and Tableau connect to and support other processing activities beyond Talent Screening.

![image.processing-activity-enabled]

![image.processing-activity-disabled]

## How Part of processing activity works

Part of Processing Activity is always defined relative to the primary record. You can use the Part of processing activity toggle in the lineage map to show only the nodes that constitute the current processing activity. Nodes that exist in the hierarchy but are not marked as Part of processing activity are hidden when the toggle is enabled. By default, the lineage map displays only nodes marked as Part of Processing Activity.

## Update the maximum node level for the data lineage map

By default, the lineage map displays nodes up to five levels downstream and one level upstream from the primary processing activity record. To display nodes beyond five downstream levels, update the `sn_privacy.nodemap.maxLevel` system property. The upstream display is always limited to one level and cannot be changed.

For more information, see [Update the maximum node level for the lineage map](../task/updating-node-level-for-lineage-map.md).

## Methods to create a lineage

You can create a lineage from the Hierarchy tab of a processing activity. For more information, see [Create a lineage for a processing activity](../task/create-a-data-lineage-for-a-processing-activity.md).

## Information displayed on the Hierarchy tab

After a relationship is created, the Hierarchy tab displays the following columns:

-   Primary node: The node for which the relationship was created.
-   Relationship: The relationship type that defines how the primary node is connected to the related node, such as Sends data to, Contains, or Depends on.
-   Related to: The node connected to the primary node by the relationship.
-   Part of processing activity: Indicates whether the application, vendor, company, entity, business process or processing activity is marked as part of the current processing activity.
-   Description: A description of the relationship.

**Parent Topic:**[Processing activities](ropa-record.md)

