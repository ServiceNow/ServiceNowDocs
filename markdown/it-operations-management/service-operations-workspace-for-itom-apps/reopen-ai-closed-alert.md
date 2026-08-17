---
title: Reopen alert closed by AI Specialist
description: Reopen an alert that the AIOps AI Specialist auto-closed as noise so it bypasses the noise classifier and runs the full investigation pipeline. Your override is honored for the alert's entire lifecycle, preserved in the audit trail, and fed back to improve future classification accuracy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/reopen-ai-closed-alert.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Use, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Reopen alert closed by AI Specialist

Reopen an alert that the AIOps AI Specialist auto-closed as noise so it bypasses the noise classifier and runs the full investigation pipeline. Your override is honored for the alert's entire lifecycle, preserved in the audit trail, and fed back to improve future classification accuracy.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## About this task

When the AI Specialist classifies an alert as noise, it closes the alert automatically. If you determine the alert is significant, reopen it. Reopening tells the system the classification was wrong, so the alert is not classified as noise again. Instead, it runs through the full investigation as if it were new and significant, and your decision helps improve future classification.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: \[Omitted image "express-list1.png"\] Alt text: Express list icon.

3.  Open an alert that was closed by AI and you want to reopen.

4.  Select the **Details** tab.

    In the Activity section, the work note states the alert is closed by an AI Specialist. The **State** field shows **Closed**.

5.  Change the **State** field value to **Reopen**.

    **Note:** Select **Reopen**, not **Open**. Only reopening an alert triggers the full re-investigation—setting it back to Open doesn't.


