---
title: Synchronize a shape to the database
description: Add a shape to a diagram. Synchronize the shape to the database by mapping the shape to an existing CI or adding a CI.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Explore Enterprise Modeling and Visualization, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Synchronize a shape to the database

Add a shape to a diagram. Synchronize the shape to the database by mapping the shape to an existing CI or adding a CI.

## Before you begin

Role required: sn\_apm.apm\_user

**Note:** You must have the Owner or Editor access to the artifact or diagram and must have read access to the shape entity.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Modeling icon \(![Modeling](../../image/eaw-image/modeling/icon-modeling-logo.png)\).

3.  Select an existing diagram from the Diagrams page.

4.  Add a shape to an existing or new diagram.

    You can observe that the unsynced icon \(![unsynced shape](../../image/eaw-image/modeling/icon-unsynced.png)\) is displayed in the shape. It means, the shape hasn’t yet synced with the ServiceNow database.

5.  Open the side panel with details for the selected shape by selecting the Open the side panel icon \(![Open side panel](../../image/eaw-image/modeling/icon-open-side-panel.png)\).

6.  Select and map an existing CI or create a CI for the shape.

    -   To map an existing CI, select the **Choose Existing** button and select a CI from the drop-down list.
    -   To create a CI, select the **Create New** button and enter the details.
7.  Send the shape or diagram for approval.

    After receiving the approval, you can see the **Commit** button to synchronize a shape or diagram, or a relationship to the database.

8.  Select **Update**.

9.  Select **Commit** to synchronize the object to the database and save the diagram.


## Result

The shape gets synced to the database.

**Parent Topic:**[Exploring Enterprise Modeling and Visualization in the EA Workspace](../../concept/eaw-concept/eaw-modeling.md)

**Related topics**  


[Create a diagram for a business capability map](eaw-modeling-bc-map.md)

[Update a business capability map](eaw-modeling-update-bc-map.md)

[Add a business capability or business application to the capability map](eaw-modeling-bcmap-add-bc-ba.md)

[Create diagram for a business hierarchy map](eaw-modeling-ba-map.md)

[Update a business application hierarchy map](eaw-modeling-update-ba-map.md)

[Share a modeling diagram](eaw-modeling-share-diagram.md)

[Commit diagram changes](eaw-modeling-sync-diagram-servicenow.md)

[Save as a new version](eaw-modeling-save-as-new.md)

[Duplicate a modeling diagram](eaw-modeling-duplicate.md)

[Submit a modeling diagram for approval](eaw-modeling-submit-for-approval.md)

[Add related records in the modeling diagram](eaw-modeling-add-related-records.md)

[Delete a shape](eaw-modeling-delete-shape.md)

