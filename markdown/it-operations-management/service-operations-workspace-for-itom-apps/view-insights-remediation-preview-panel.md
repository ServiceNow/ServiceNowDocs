---
title: View alert insights and remediation in Preview panel
description: Resolve alerts more quickly by reviewing AI-generated insights and recommended remediation in the Preview panel and acting on them without navigating to the alert record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-operations-workspace-for-itom-apps/view-insights-remediation-preview-panel.html
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View alert insights and remediation in Preview panel

Resolve alerts more quickly by reviewing AI-generated insights and recommended remediation in the Preview panel and acting on them without navigating to the alert record.

## Before you begin

Verify you have the Now Assist for IT Operations Management \(ITOM\) plugin installed on your instance. For more information about installing Now Assist plugins, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

Role required: evt\_mgmt\_admin or evt\_mgmt\_operator

## About this task

The alert insights feature investigates alerts, summarizes alert-related reports, and stores structured insights with key findings. It also recommends remediation steps that you can activate or dismiss directly from the Preview panel.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \[Omitted image "express-list1.png"\].

3.  Select the alert for which you want to view alert insights.

    The Preview panel opens with the **Insights** tab selected by default.

4.  If the **Insights** tab shows a `Waiting for approval` message, select **Approve** to start the analysis.

    The alert insights appear once the analysis completes.

5.  Under **Next steps**, view the recommended remediation steps.

    \[Omitted image "el-view-insights-remediation.png"\] Alt text: Preview panel showing recommended remediation steps.

6.  Under **Primary action**, select **Dismiss** or **Activate** for a remediation step.

    When you select **Activate**, ServiceNow runs the recommended remediation action for the alert. When you select **Dismiss**, the recommendation is discarded and no action is taken.


