---
title: Review AI generated alert information and insights in Express List
description: Access alert information in Express List that is consolidated autonomously by AI skills and agents. Use the AI insights badge, column, and filter to monitor alert statuses and review of AI-generated insights.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage alerts autonomously agentic workflow, Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Review AI generated alert information and insights in Express List

Access alert information in Express List that is consolidated autonomously by AI skills and agents. Use the AI insights badge, column, and filter to monitor alert statuses and review of AI-generated insights.

## Before you begin

For this feature, you must have Now Assist for IT Operations Management \(ITOM\) installed on your instance. For more information about installing Now Assist plugins, see Install Now Assist plugins.

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator

## About this task

The manage alerts autonomously workflow investigates alerts, summarizes alert-related reports, and stores structured insights with key findings for use in Express List. For more information about the manage alerts autonomously agentic workflow, see [Manage alerts autonomously agentic workflow](../concept/itom-autonomous-operator-workflow.md).

**Note:** Currently, Now Assist for ITOM only supports tag-based, CMDB, Log Analytics, Mixed, Automated, and Network Traffic-based alert groups. For all other alert group types, it only analyzes the parent alert.

There are several ways to explore AI insights in Express List.

-   Quickly review if alerts have been processed by checking for the AI insights badge ![](../image/ai-insights-icon.png).
-   Search for specific information and key words in the Insights column. To add the column, see [Add or modify Express List columns](../../service-operations-workspace-itom/task/edit-list-columns-el.md) for more information.
-   Filter for information by using the **Insights** filter attribute in the filter panel.
-   Review **AI insights** in the preview panel or the alert record.

These options present differently, depending on whether the workflow is configured for automatic or manual execution.

-   When the workflow operates automatically, alerts are addressed as they’re created and AI insight information is displayed in Express List.
-   When the workflow operates manually, you must manually generate AI insights. For more information, see details in the following procedure.

For information about configuring this workflow, see [Configure the manage alerts autonomously agentic workflow](configure-manage-alerts-autonomously-workflow.md).

## Procedure

1.  Navigate to **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the Express List icon ![](../../event-management/image/express-list1.png).

3.  Review the AI insights through the following options.

<table id="choicetable_qzt_n1y_thc"><thead><tr><th align="left" id="d123224e213">

Review AI insights

</th><th align="left" id="d123224e216">

Procedure

</th></tr></thead><tbody><tr><td id="d123224e222">

**Check for the AI Insights badge for alert status**

</td><td>

-   If the AI insights icon ![](../image/ai-insights-icon.png) is visible next to the check box, insights are available for that alert.
-   If insights aren't available for an alert, you can initiate the process manually. Details for generating insights are in the following options.


</td></tr><tr><td id="d123224e245">

**Search for alerts with AI Insights information and key words**

</td><td>

Search for content with the free text search. For more information, see [Find alert records in Express List using text search](../../service-operations-workspace-itom/task/el-free-text-search.md).

</td></tr><tr><td id="d123224e261">

**Filter using AI Insights filter attribute**

</td><td>

Filter using the **Insights** attribute with a minimum string of two characters. For more information, see [Filtering the alert display in the Express List pane](../../service-operations-workspace-itom/concept/filter-express-list.md).

</td></tr><tr><td id="d123224e280">

**Review AI insights in the preview panel**

</td><td>

1.  In the alerts list, select an alert by selecting the check box or the information icon ![Information icon.](../../event-management/image/info.png) next to the alert.
2.  -   In the **Insights** tab, review **AI insights**.
-   If data isn’t available for this alert, you can initiate the process by selecting **Generate**.


</td></tr><tr><td id="d123224e323">

**Review AI Insights in the alert record overview**

</td><td>

1.  In the alerts list, select an alert number to open the alert record.

The **Overview** tab is selected by default.

2.  -   If data is available, you can review the **AI insights** summary in the Summary section.
-   If data isn’t available for this alert, you can initiate the process by selecting **Generate**.


</td></tr></tbody>
</table>
