---
title: Reassign alert after AI processing
description: Learn how an alert assigned to an operator and handled by the AI Specialist is automatically reassigned to the original operator after AI investigation or remediation completes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/assign-alert-ai-specialist.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Use, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Reassign alert after AI processing

Learn how an alert assigned to an operator and handled by the AI Specialist is automatically reassigned to the original operator after AI investigation or remediation completes.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## About this task

The AI Specialist takes an alert only when it is not already assigned to a human operator. If an alert already has an assignee, the AI Specialist does not run on it automatically. When the AI Specialist does take an assigned alert—through an alert rule or a manual remediation/insight trigger—it records the original assignee. The alert can then be returned after processing. If the alert is closed as noise, it is not reassigned back to the operator.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: \[Omitted image "express-list1.png"\] Alt text: Express list icon.

3.  In the alerts list, select an alert number to open the alert.

    On the **Details** tab, in the **Assigned to** field, note the name of the operator the alert is assigned to.

4.  On the **Overview** tab, where it shows `Waiting for approval`, select **Approve** to let the AI Specialist analyze the alert.

    The AI Specialist workflow starts and the **Assigned to** field changes to AI Specialist. After the workflow completes, the field resets to the original operator—unless the alert was closed as noise or manually reassigned.


