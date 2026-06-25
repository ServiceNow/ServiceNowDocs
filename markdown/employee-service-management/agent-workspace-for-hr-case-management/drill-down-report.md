---
title: Enable a detailed data display within a report
description: Enable users to visualize a subset of report data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/agent-workspace-for-hr-case-management/drill-down-report.html
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [UI Builder for Agent Workspace for HR Case Management, Setting up Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Enable a detailed data display within a report

Enable users to visualize a subset of report data.

## Before you begin

Role required: sn\_hr\_agent\_ws.admin and sn\_hr\_core.basic

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **UI Builder for Agent Workspace for HR Case Management**.

2.  Select your variant.

3.  Select the container containing your report.

4.  In the Configuration panel, select **Data update**.

5.  Turn on the **Enable drilldown** option.

    \[Omitted image "enable-drilldown.png"\] Alt text: Drilldown toggle switch

6.  In the Events panel, select **+Add event handler** to map the data that is displayed when the user drills down on the report.

    \[Omitted image "event-handler.png"\] Alt text: Event handler

7.  In the **Search item** field, enter `Open cases - simple list page`.

8.  Select **Open cases - simple list page**.

9.  Select **Add**.

10. Select **Save**.


**Parent Topic:**[UI Builder for Agent Workspace for HR Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/agent-workspace-for-hr-case-management/uib-aws.md)

**Related topics**  


[Create a landing page variant]()

[Configure quick links in Agent Workspace for HR Case Management]()

[Reorder the navigation pane modules in HR Agent Workspace]()

