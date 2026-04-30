---
title: Duplicate a modeling diagram
description: You can make a copy of an existing diagram that you created and modify the duplicate diagram according to your requirement.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with Enterprise Modeling and Visualization, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Duplicate a modeling diagram

You can make a copy of an existing diagram that you created and modify the duplicate diagram according to your requirement.

## Before you begin

Role required: Role required: sn\_apm.apm\_user and Owner or Editor access to the artifact or diagram

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(![Enterprise Modeling and Visualization icon.](../../image/eaw-image/modeling/icon-modeling-logo.png)\).

3.  Select an existing diagram from the Diagrams page.

4.  Select the More actions menu ![More actions menu](../../image/icon-three-dot-menu-eaw.png).

5.  Select **Duplicate**.

6.  Enter a name for the diagram.

    On duplicating a business process map, the value in the **Link to business process** field in the **Duplicate** pop-up window is selected by default, based on the status of the business process associated with the original business process map.

    -   If the original business process isn’t committed to the database:
        -   The default selection in the **Link to business process** field is **New**.
        -   You can rename the business process in the **Name of new business process** field.
    -   If the original business process exists in the database:
        -   The default selection in the **Link to business process** field is **Existing**.
        -   You can choose a different business process using the **Select existing business process** field.
    You can change the default values in the **Link to business process** field according to your requirement.

7.  Select **Duplicate**.


## Result

A duplicate diagram is created.

**Parent Topic:**[Working with Enterprise Modeling and Visualization](../../concept/eaw-concept/eaw-work-with-ent-model-and-visual.md)

**Related topics**  


[Create a diagram for a business capability map](eaw-modeling-bc-map.md)

[Update a business capability map](eaw-modeling-update-bc-map.md)

[Add a business capability or business application to the capability map](eaw-modeling-bcmap-add-bc-ba.md)

[Create diagram for a business hierarchy map](eaw-modeling-ba-map.md)

[Update a business application hierarchy map](eaw-modeling-update-ba-map.md)

[Add related records in the modeling diagram](eaw-modeling-add-related-records.md)

[Share a modeling diagram](eaw-modeling-share-diagram.md)

[Commit diagram changes](eaw-modeling-sync-diagram-servicenow.md)

[Save as a new version](eaw-modeling-save-as-new.md)

[Submit a modeling diagram for approval](eaw-modeling-submit-for-approval.md)

[Synchronize a shape to the database](eaw-modeling-sync-shape.md)

[Delete a shape](eaw-modeling-delete-shape.md)

