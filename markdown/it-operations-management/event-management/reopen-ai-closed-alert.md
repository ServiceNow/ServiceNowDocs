---
title: Reopen alert closed by AI Specialist
description: Reopen an alert that the AIOps AI Specialist auto-closed as noise so it bypasses the noise classifier and runs the full investigation pipeline. Your override is honored for the alert's entire lifecycle, preserved in the audit trail, and fed back to improve future classification accuracy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/reopen-ai-closed-alert.html
release: brazil
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Manage alert states in Express List, Assigning and managing alerts, Express List, Event Management, ITOM AIOps, IT Operations Management]
---

# Reopen alert closed by AI Specialist

Reopen an alert that the AIOps AI Specialist auto-closed as noise so it bypasses the noise classifier and runs the full investigation pipeline. Your override is honored for the alert's entire lifecycle, preserved in the audit trail, and fed back to improve future classification accuracy.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## About this task

When the AI Specialist classifies an alert as noise, it closes the alert automatically. If you determine the alert is significant, reopen it. Reopening tells the system the classification was wrong, so the alert is not classified as noise again. Instead, it runs through the full investigation as if it were new and significant, and your decision helps improve future classification.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \[Omitted image "express-list1.png"\].

3.  Open an alert that was closed by AI and you want to reopen.

    When an alert is auto-closed by the AIOps AI Specialist, its reasoning appears under the **Overview** tab in the Summary section. If you determine the alert is significant, reopen it. The alert can be reopened by selecting the **Reopen** link provided following the reasoning or you can reopen the alert from the **Details** tab as shown in the procedure.

4.  Select the **Details** tab.

    In the Activity section, the work note states the alert is closed by an AI Specialist. The **State** field shows **Closed**.

5.  Change the **State** field value to **Reopen**.

    **Note:** Select **Reopen**, not **Open**. Reopen is the state transition the system watches for to trigger the classifier bypass and full investigation pipeline. Setting the state to **Open** does not register as an operator override of the AI close, so the alert would not be guaranteed the bypass-and-reinvestigate treatment.


