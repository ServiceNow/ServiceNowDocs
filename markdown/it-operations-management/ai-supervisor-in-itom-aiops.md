---
title: Overseeing AIOps AI Specialist in Service Operations Workspace
description: The AIOps Supervisor home page helps supervisors review operational workload, monitor AIOps AI Specialist activity, and review alerts closed by AIOps AI Specialist in Service Operations Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/ai-supervisor-in-itom-aiops.html
release: australia
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 3
keywords: [AIOps Supervisor, AIOps AI Specialist, ITOM AIOps, Service Operations Workspace, Event Management]
breadcrumb: [Manage the AI specialist, AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# Overseeing AIOps AI Specialist in Service Operations Workspace

The AIOps Supervisor home page helps supervisors review operational workload, monitor AIOps AI Specialist activity, and review alerts closed by AIOps AI Specialist in Service Operations Workspace.

## AIOps Supervisor

AIOps Supervisor is an elevated Event Management operator role, letting supervisors oversee the AIOps AI Specialist's work, handle only alerts requiring human attention, and run its recommended remediation actions.

You can access the AIOps Supervisor home page with the Event Management Operator `evt_mgmt_operator` role.

**Note:** The AI Specialist section appears on the AI Supervisor home page whenever you enable the Autonomous Operator Workflow, even if you have not activated AI Specialist.

## AIOps Supervisor home page scope

The home page shows activity for the AIOps AI Specialist assigned to your assignment group. It enables you to review alerts closed by AIOps AI Specialist and investigate alerts that need your attention during your shift. The page shows information for the last 24 hours. Only one AIOps AI Specialist can be active for each assignment group.

The home page provides a consolidated view of AIOps AI Specialist activity over the last 24 hours and identifies the alerts that require human attention.

\[Omitted image "ai-supervisor-your-work-tab.png"\] Alt text: Sample AIOps Supervisor home page - Your work tab

Highlighted work that may require your attention in the **Needs your attention** section includes:

-   Critical alerts for your team
-   Open alerts assigned to the team
-   Open alerts assigned to you
-   Open incidents assigned to you

This view helps you focus on the most important alerts you should handle first without your having to check multiple lists.

The **AI supervision overview** section provides further information on AI specialist activities.

|Item|Description|
|----|-----------|
|**Time saved by AI activity**|Estimated time saved by AIOps AI Specialist activity. The value is calculated by multiplying alerts closed by AIOps AI Specialist by the configured time saved per closed alert. This is added to alerts analyzed by AIOps AI Specialist multiplied by the configured time saved per analyzed alert.|
|**Alerts processed**|Number of alerts processed by AIOps AI Specialist.|
|**Currently processing**|Number of alerts that AIOps AI Specialist is processing.|
|**Recent activity**|Recent alerts being analyzed by AIOps AI Specialist.|
|**Closed by AI to review**|Alerts that were closed by AIOps AI Specialist and are ready for review.|

## AI Supervision information

The **AI Supervision** tab shows activity for the AIOps AI Specialist assigned to your assignment group.

|Item|Description|
|----|-----------|
|**Processed by AIOps AI Specialist**|Number of alerts processed by AIOps AI Specialist.|
|**Closed by AIOps AI Specialist to review**|Number of alerts closed by AIOps AI Specialist and ready for review.|
|**In process by AIOps AI Specialist**|Number of alerts currently being processed by AIOps AI Specialist.|
|**Closed by AIOps AI Specialist alerts list**|Alerts closed by AIOps AI Specialist. The list includes alert details such as number, description, and source.|
|**Alert details** pane|Details for the selected alert.|
|**Insights**|AI-generated summary and context for the selected alert.|
|**Info**|Additional information about the selected alert.|
|**Activity**|Activity history for the selected alert.|

AIOps AI Specialist processes alerts based on its configured scope. It can help with triage, investigation, impact analysis, and remediation recommendations. The home page shows AIOps AI Specialist activity as part of the team's operational workload.

-   **[Review work on the AIOps Supervisor home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/review-work-on-the-aiops-supervisor-home-page.md)**  
Review alerts, incidents, and AIOps AI Specialist activity across selected assignment groups on the AIOps Supervisor home page in Service Operations Workspace.

**Parent Topic:**[Manage the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/manage-the-ai-specialist.md)

