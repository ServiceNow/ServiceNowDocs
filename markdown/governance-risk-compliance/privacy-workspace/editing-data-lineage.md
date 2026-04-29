---
title: Edit a lineage
description: Edit an existing lineage relationship to update the relationship type, description, or key relationship status of a connected node.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a lineage for a processing activity, Use, Privacy Management, Governance, Risk, and Compliance]
---

# Edit a lineage

Edit an existing lineage relationship to update the relationship type, description, or key relationship status of a connected node.

## Before you begin

Role required: Privacy analyst, Privacy manager, Privacy admin

## About this task

You can edit a relationship from the lineage map by selecting the arrow between two nodes, or by navigating to the related node record in the **Hierarchy** tab list.

**What you can edit:**

-   Relationship type: You can change the relationship type, but only within the same data flow direction. A downstream relationship type can only be changed to another downstream relationship type. An upstream relationship type can only be changed to another upstream relationship type. You cannot change the direction of data flow, as the source and target of a relationship cannot be reversed after it has been created.
-   Description: You can update the description of the relationship.
-   Part of processing activity: You can enable or disable or disable Part of Processing Activity for a relationship, subject to the hierarchy rules.

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace** &gt; **Processing activities** &gt; **All processing activities**.

2.  Select the processing activity record.

3.  Navigate to the **Hierarchy** tab.

4.  Select **View lineage map** to open the graphical view.

5.  Select the arrow between the two nodes and select **View/Edit relationship**.

    The edit panel opens. You can also single-click the arrow to see more information before deciding to edit.

6.  Modify the Relationship type, Description, or Part of processing activity fields as needed.

7.  Select **Save** to save the changes.


**Parent Topic:**[Create a lineage for a processing activity](create-a-data-lineage-for-a-processing-activity.md)

