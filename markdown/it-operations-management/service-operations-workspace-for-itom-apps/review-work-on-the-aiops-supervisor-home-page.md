---
title: Review work on the AIOps Supervisor home page
description: Review alerts, incidents, and AIOps AI Specialist activity across selected assignment groups on the AIOps Supervisor home page in Service Operations Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/review-work-on-the-aiops-supervisor-home-page.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-08-23"
reading_time_minutes: 2
keywords: [AIOps Supervisor, AIOps AI Specialist, Service Operations Workspace, Event Management, evt\_mgmt\_operator]
breadcrumb: [Overseeing AIOps AI Specialist in Service Operations Workspace, Explore, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Review work on the AIOps Supervisor home page

Review alerts, incidents, and AIOps AI Specialist activity across selected assignment groups on the AIOps Supervisor home page in Service Operations Workspace.

## Before you begin

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the **Service Operations Workspace** navigation menu, select **Home**.

    If the AIOps Supervisor home page does not appear, a customized home page might be configured. To show the AIOps Supervisor home page, revert to the default home page. For more information, see [Customize Service Operations Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/configure-service-operations-workspace-landing-page.md).

3.  Set the assignment group scope.

    1.  Open the assignment group selector.

    2.  Select one or more assignment groups.

        To include alerts that do not have an assignment group, select **Unassigned alerts**.

    The assignment group selection persists during the session.

4.  Review the alerts that require human attention in the **Needs your attention** section.

5.  Select the relevant widget to view detailed information.

    The available information is:

    -   **Team's critical alerts**
    -   **Team's open alerts**
    -   **Your open alerts**
    -   **Your open incidents**
    The record cards update based on the widget that you select.

6.  Review record information.

    1.  View a summary of the record on an alert or incident card.

        Each card includes the following data:

        -   Alert or incident number
        -   Short description
        -   Severity
        -   Affected configuration item
        -   Source
        -   How long the record has been open
        -   Suggested remediation action, if found by AI
    2.  Select an alert or incident card to view details of the record.

    3.  Select **View all**.

        For alerts, Express List opens with the relevant filter applied. For incidents, the incident list opens.

    4.  Use Express List to continue reviewing the filtered records.

7.  If the **AI supervision overview** section appears, review AIOps AI Specialist activity.

    The section appears when at least one selected assignment group has an active AIOps AI Specialist. Review the time saved, alerts processed, alerts currently in progress, auto-closed alerts, and recent activity.

8.  Open the relevant AIOps AI Specialist alert list.

    -   To review alerts processed by AIOps AI Specialist, select the **Alerts processed** count. The **Processed by AIOps specialist** list opens.
    -   To review alerts that AIOps AI Specialist is currently processing, select the **Currently in progress** count. The **Currently in progress by AIOps specialist** list opens.
    -   To review alerts that AIOps AI Specialist auto-closed, select **Review**. The **Closed by AIOps specialist** list opens.
9.  Select an alert in the list to review its details.

    Depending on the processing state, the preview panel provides information such as **Insights**, **Info**, and **Probable cause**.

10. If an alert that AIOps AI Specialist auto-closed requires follow-up, select **Reopen**.

    For more information, see [Reopen alert closed by AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/reopen-ai-closed-alert.md).


