---
title: Create a lineage for a processing activity
description: Establish a lineage to visualize data consumption, sharing, and the associated risks for a processing activity. Each processing activity involves multiple information objects classified as personal information. These objects exchange data with various other entities, making it essential to establish a lineage or hierarchy that tracks where personal data is shared.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Create a lineage for a processing activity

Establish a lineage to visualize data consumption, sharing, and the associated risks for a processing activity. Each processing activity involves multiple information objects classified as personal information. These objects exchange data with various other entities, making it essential to establish a lineage or hierarchy that tracks where personal data is shared.

## Before you begin

The processing activity must be in Discover state or later. If the processing activity is in New state, move it to Discover before proceeding.

Role required: Privacy analyst, Privacy manager, Privacy admin

## About this task

Establish a lineage to visualize data consumption, sharing, and the associated risks for a processing activity. Each processing activity could involve multiple entities such as vendors, applications, and systems that make up the processing activity. These vendors, applications, and systems share data with each other, making it essential to establish a lineage that tracks where personal data is shared. This helps mitigate privacy-related risks.

You add lineage relationships from the **Hierarchy** tab using the **Add** button. The Add screen is a two-step flow. In the first step you define the relationship, and in the second step you provide the relationship details.

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace** &gt; **Processing activities** &gt; **All processing activities**.

2.  Navigate to the **Hierarchy** tab.

3.  Select **Add**.

4.  In the Primary node field, review the pre-selected record.

    This field is automatically set to the processing activity you have open. You can change the primary node to any other node that has been linked with the processing activity.

5.  In the **Relationship Type** field, select the relationship type that describes how this processing activity relates to the node you want to add.

    Select from the following options:

    1.  Depends on: The primary node depends on the related node for data. Data flows from the related node to the primary node.
    2.  Contains: The primary node contains the related node. Data flows from the primary node to the related node.
    3.  Contained by: The primary node is contained by the related node. Data flows from the related node to the primary node.
    4.  Sends data to: The primary node sends data to the related node. Data flows from the primary node to the related node.
    5.  Receives data from: The primary node receives data from the related node. Data flows from the related node to the primary node.
    6.  Used by: The primary node is used by the related node. Data flows from the primary node to the related node.
6.  In the **Related Node Type** field, select the type of entity you want to add.

    The available types are Processing Activity, Entity, Business Application, Business Process, Business Service, Company, and Vendor.

7.  In the Related Node field, select from the available related nodes list and then select **Next**.

    You can add more than one related node.

8.  For each related node, set the following options:

    -   Part of processing activity: This option is enabled by default. Keep it selected if this is part of the current processing activity.
    -   Description: Enter a description of the relationship for this node.
    -   Copy details: If you have added multiple nodes and want to apply the description of one node to all other nodes, select Copy Details on that node.
    -   Remove: To remove a node before saving, select the remove icon next to that node.
9.  Select **Add**.


## Result

The new node appears in the **Hierarchy** tab list. When you select the View lineage map, the node appears in the graphical view. If the related node is itself a processing activity with existing relationships, those connections also appear in the map.

-   **[Edit a lineage](editing-data-lineage.md)**  
Edit an existing lineage relationship to update the relationship type, description, or key relationship status of a connected node.
-   **[Delete a lineage](delete-data-lineage.md)**  
Delete a lineage to remove a specific connection or node from the hierarchy of a processing activity.
-   **[Update the maximum node level for the lineage map](updating-node-level-for-lineage-map.md)**  
Update the `sn_privacy.nodemap.maxLevel system` property to control how many node levels are visible on the lineage map.

**Parent Topic:**[Using Privacy Management](../concept/using-privacy-mgmt.md)

