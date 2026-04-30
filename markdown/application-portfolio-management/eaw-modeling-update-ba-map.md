---
title: Update a business application hierarchy map
description: Modify an existing business application hierarchy map by adding or removing shapes and relationships.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with business hierarchy map, Working with Enterprise Modeling and Visualization, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Update a business application hierarchy map

Modify an existing business application hierarchy map by adding or removing shapes and relationships.

## Before you begin

Role required: sn\_apm.apm\_user

**Note:** You must have the Owner or Editor access to the artifact or diagram.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(![Enterprise Modeling and Visualization icon](../../image/eaw-image/modeling/icon-modeling-logo.png)\).

3.  Open an existing business hierarchy map artifact from the **Diagrams** page.

4.  Select the newly added shape and select the Open the side panel icon \(![Open side panel](../../image/eaw-image/modeling/icon-open-side-panel.png)\) to open the details panel for the selected shape in the canvas.

5.  Select a shape in the diagram to see the following options:

    -   Side panel icon \(![Open side panel](../../image/eaw-image/modeling/icon-open-side-panel.png)\) to update the details of a record.
    -   Add related records icon \( ![Add related records](../../image/eaw-image/modeling/icon-add-related-records.png)\) to add entities and relationship.
    -   More Actions context menu \(![More actions menu](../../image/eaw-image/eaw-icon-menu.png)\) to see options for adding relationship or deleting a shape from the canvas.
6.  Select **Commit changes** to synchronize the diagram to the database.

    This option is available only when the diagram is approved. For more information, see [Synchronize a shape to the database](eaw-modeling-sync-shape.md).

7.  Select **Share** to share the diagram with individuals or groups.

    For more information, see [Share a modeling diagram](eaw-modeling-share-diagram.md).

8.  Select the More Actions menu \(![More actions menu.](../../image/icon-three-dot-menu-eaw.png)\) to perform the following actions:

    -   **Save as new version**: Select this option to create a version for the selected diagram. The version number is automatically added in the Version number field, and it isn’t editable. For more information, see [Save as a new version](eaw-modeling-save-as-new.md).
    -   **Duplicate**: Select this option to duplicate the diagram. For more information, see [Duplicate a modeling diagram](eaw-modeling-duplicate.md).
    -   **Submit for approval**: Select this option to submit the diagram for approval. The approval process can be done through a configured workflow. By default, the approval request is submitted to the Enterprise Architect group. For more information, see [Submit a modeling diagram for approval](eaw-modeling-submit-for-approval.md).

**Parent Topic:**[Working with business hierarchy map](../../concept/eaw-concept/eaw-work-with-ba-map.md)

**Related topics**  


[Create a diagram for a business capability map](eaw-modeling-bc-map.md)

[Update a business capability map](eaw-modeling-update-bc-map.md)

[Add a business capability or business application to the capability map](eaw-modeling-bcmap-add-bc-ba.md)

[Create diagram for a business hierarchy map](eaw-modeling-ba-map.md)

