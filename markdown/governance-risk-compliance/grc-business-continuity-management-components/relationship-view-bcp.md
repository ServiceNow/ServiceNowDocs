---
title: Visualize 360° relationships for the BCP
description: Visualize the 360° relationships for a business continuity plan \(BCP\) and its associated entities in BCM UIB Workspace. You can access the 360° view at any time while working on the business continuity plan.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Visualize 360° relationships for the BCP

Visualize the 360° relationships for a business continuity plan \(BCP\) and its associated entities in BCM UIB Workspace. You can access the 360° view at any time while working on the business continuity plan.

## Before you begin

Role required: sn\_bcm.program\_manager, sn\_bcm.planner

## About this task

The configurations for the 360° view are stored in **360° View Configurations** &gt; **Configure 360° Views**. If you have the BCM administrator role, you can configure the relationships for the records in **360° View Configurations** &gt; **Relationship Registries**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Planning** and select a record from the list.

    The business continuity plan record is displayed.

3.  Select **360° view**.

    The example shows the 360° view of a business continuity plan and its details.

    ![360° view for a BCP.](../image/360-bcp.png)

    -   **Name**: Name of the business continuity plan such as Customer Support Continuity Plan. You can select the business continuity plan to view its details.
    -   **BCM lead**: Assigned BCM lead for the business continuity plan.
    -   **Scope**: Scope of the business continuity plan such as **Related plans**.
    -   **Events**: Events that are associated with the business continuity plan such as **Ongoing events**.
    -   **Include**: Entities that are associated with the business continuity plan such as **Loss scenario**, **Documentation**, and **Recovery tasks** as shown in the example.
    The example shows the 360° relationship view for the Customer Support Continuity Plan and its related entities. When you select the **Loss scenario** capsule in the 360° view, the details of the associated loss scenarios for the Customer Support Continuity Plan are displayed in the Loss scenario panel on the right.

    ![360-view-for-a-loss-scenario.](../image/360-bcp-loss-scenario.png)

4.  To navigate to the plan again, select the plan or list view in the breadcrumb navigation.


**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

