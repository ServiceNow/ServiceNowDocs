---
title: View 360° relationships for exercises and crises
description: Visualize the 360° relationships for an exercise or a crisis event and the associated entities in BCM UIB Workspace. You can access the 360° view at any time while creating an exercise and a crisis event.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View 360° relationships for exercises and crises

Visualize the 360° relationships for an exercise or a crisis event and the associated entities in BCM UIB Workspace. You can access the 360° view at any time while creating an exercise and a crisis event.

## Before you begin

Role required: sn\_bia.bia\_admin, sn\_bcm.program\_manager, sn\_bcm.planner

## About this task

The configurations for the 360° view are stored in **360° View Configurations** &gt; **Configure 360° Views**. If you have the BCM administrator role, you can configure the relationships for the records in **360° View Configurations** &gt; **Relationship Registries**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercise**.

2.  Select a record from the list.

    The exercise event record is displayed. The same procedure applies for a crisis event.

3.  Select **360° view** in the event record.

    The 360° view for the selected event is displayed as shown in the example.

    ![360-view-events.](../image/360-ex-view.png)

    The 360° view for the selected event shows these details:

    -   **Activated plans**: Activated plans that are associated with the assets.
    -   **Assets**: Assets that are impacted due to the event.
    -   **Tasks**: Tasks that are associated with the event.
    When you select the **Assets** capsule in the 360° view, the details of the assets for the event are displayed in the **Assets** panel on the right as shown in the example.

4.  Select the event or list view in the breadcrumb navigation to open the original event record.


**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)

