---
title: Add related records in the modeling diagram
description: Fetch and add a related record to the selected shape in a diagram.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with Enterprise Modeling and Visualization, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add related records in the modeling diagram

Fetch and add a related record to the selected shape in a diagram.

## Before you begin

Role required: sn\_apm.apm\_user and Owner or Editor access to the artifact or diagram

## About this task

You can add both upstream and downstream related entities to a shape in a diagram.

-   Upstream entities appear as the parents of a selected shape. They represent inputs, dependencies, or higher-level components that influence the selected shape. For example, for a business process, an upstream entity can be a business capability.
-   Downstream entities appear as children of the selected shape. They represent the outputs or consequences that are influenced by the selected shape. For example, for a business capability, a downstream entity can be a business application.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(![Enterprise Modeling and Visualization icon](../../image/eaw-image/modeling/icon-modeling-logo.png)\).

3.  Select an existing diagram from the Diagrams page.

4.  Select a shape in the diagram and then open the context menu and then the More Actions menu \(![More actions menu icon](../../image/eaw-image/eaw-icon-menu.png)\).

5.  Open the **Add related records** pop-up window by selecting the Add related records icon \(![Add related records icon](../../image/eaw-image/modeling/icon-add-related-records.png)\).

6.  Select the entities that you want to add to the diagram.

    -   Select the Expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Upstream** or **Downstream** to view the list of available related entities.
    -   Select the check box next to the relevant entity.
7.  Select **Add**.


## Result

The selected entities are added to the diagram for the object.

**Parent Topic:**[Working with Enterprise Modeling and Visualization](../../concept/eaw-concept/eaw-work-with-ent-model-and-visual.md)

**Related topics**  


[Share a modeling diagram](eaw-modeling-share-diagram.md)

[Commit diagram changes](eaw-modeling-sync-diagram-servicenow.md)

[Save as a new version](eaw-modeling-save-as-new.md)

[Duplicate a modeling diagram](eaw-modeling-duplicate.md)

[Submit a modeling diagram for approval](eaw-modeling-submit-for-approval.md)

[Synchronize a shape to the database](eaw-modeling-sync-shape.md)

[Delete a shape](eaw-modeling-delete-shape.md)

