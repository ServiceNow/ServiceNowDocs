---
title: Overseeing AIOps AI Specialist in Service Operations Workspace
description: The AIOps Supervisor home page helps supervisors review operational workload across selected assignment groups and monitor AIOps AI Specialist activity in Service Operations Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/ai-supervisor-in-itom-aiops.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2026-08-23"
reading_time_minutes: 2
keywords: [AIOps Supervisor, AIOps AI Specialist, ITOM AIOps, Service Operations Workspace, Event Management]
breadcrumb: [Explore, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Overseeing AIOps AI Specialist in Service Operations Workspace

The AIOps Supervisor home page helps supervisors review operational workload across selected assignment groups and monitor AIOps AI Specialist activity in Service Operations Workspace.

## AIOps Supervisor

AIOps Supervisor is an elevated Event Management operator role that lets you oversee the AIOps AI Specialist's work, handle alerts that require human attention, and run recommended remediation actions.

You can access the AIOps Supervisor home page with the Event Management Operator `evt_mgmt_operator` role.

## AIOps Supervisor home page scope

The assignment group selector defines the team scope shown on the home page. You can select one or more assignment groups to view alerts from those groups together. The selector lists the assignment groups available to you and reflects the active selection.

You can also include **Unassigned alerts** to view alerts that don't have an assignment group. The **Unassigned alerts** option appears after the available assignment groups.

Your selection persists during the session. The page shows information for the last 24 hours. Only one AIOps AI Specialist can be active for each assignment group.

When at least one selected assignment group has an active AIOps AI Specialist, the home page includes the **AI supervision overview** and AIOps AI Specialist activity. When none of the selected assignment groups has an active AIOps AI Specialist, AI supervision content doesn't appear.

\[Omitted image "ai-supervisor-your-work-tab.png"\] Alt text: AIOps Supervisor home page with alert workload and AI supervision information

## Needs your attention

The **Needs your attention** section highlights operational work that might require your attention. It includes:

-   **Team's critical alerts**
-   **Team's open alerts**
-   **Your open alerts**
-   **Your open incidents**

The home page alert lists reflect the active assignment group selection. When **Unassigned alerts** is selected, the lists can also include alerts that don't have an assignment group.

This view helps you focus on alerts that require attention without checking multiple alert lists.

## AI supervision overview

The **AI supervision overview** section provides information about AIOps AI Specialist activity when at least one selected assignment group has an active AIOps AI Specialist.

|Item|Description|
|----|-----------|
|**Time saved by AIOps AI specialist activity**|Estimated time saved by AIOps AI Specialist activity. The value is calculated by multiplying alerts closed by AIOps AI Specialist by the configured time saved per closed alert. This value is added to alerts analyzed by AIOps AI Specialist multiplied by the configured time saved per analyzed alert.|
|**Alerts processed**|Number of alerts processed by AIOps AI Specialist.|
|**Currently in progress**|Number of alerts that AIOps AI Specialist is processing.|
|Auto-closed alerts|Number of alerts that AIOps AI Specialist closed automatically and that are available for review.|
|**Recent activity**|Recent AIOps AI Specialist activity for alerts.|

## AIOps AI Specialist alert lists

The **AI supervision overview** provides access to alert lists organized by AIOps AI Specialist processing state:

-   **Processed by AIOps specialist** contains alerts processed by AIOps AI Specialist.
-   **Closed by AIOps specialist** contains alerts closed by AIOps AI Specialist and available for review.
-   **Currently in progress by AIOps specialist** contains alerts that AIOps AI Specialist is currently processing.

The alert lists provide filters and details for the selected alert. Alert details can include **Insights**, **Info**, and **Probable cause** information generated during AIOps AI Specialist processing.

AIOps AI Specialist processes alerts based on its configured scope. It can assist with triage, investigation, impact analysis, and remediation recommendations. The AIOps Supervisor home page presents this activity as part of the team's operational workload.

