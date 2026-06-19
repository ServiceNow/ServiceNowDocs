---
title: Review AI generated alert information and insights in Express List
description: Access alert information in Express List that is consolidated autonomously by AI skills and agents. Use the AI insights badge, column, and filter to monitor alert statuses and review of AI-generated insights.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/use-ai-insights-express-list.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-12-22"
reading_time_minutes: 4
breadcrumb: [Manage alerts autonomously agentic workflow, Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Review AI generated alert information and insights in Express List

Access alert information in Express List that is consolidated autonomously by AI skills and agents. Use the AI insights badge, column, and filter to monitor alert statuses and review of AI-generated insights.

## Before you begin

For this feature, you must have Now Assist for IT Operations Management \(ITOM\) installed on your instance. For more information about installing Now Assist plugins, see .

Role masking enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

\[Optional\] Additional configuration is required for some skills used in the agentic workflow:

-   **Observability skills**: Configure the relevant observability skills to surface data from observability tools integrated with Event Management. See .
-   **Log analytics skills**: Install and configure Health Log Analytics to enable analysis of log analytics alerts. See [Configuring Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-configuring.md).
-   **Service health skill**: Install and configure Service Observability and activate the analyze service health skill to automatically surface insights about service health in an alert. See [Install Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-observability/install-service-observability.md) and [Activate the analyze service health skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/activate-the-analyze-service-health-skill.md) for more information.

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator

## About this task

The manage alerts autonomously workflow investigates alerts, summarizes alert-related reports, and stores structured insights with key findings for use in Express List. For more information about the manage alerts autonomously agentic workflow, see [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md).

**Note:** Currently, Now Assist for ITOM only supports tag-based, CMDB, Log Analytics, Mixed, Automated, and Network Traffic-based alert groups. For all other alert group types, it only analyzes the parent alert.

There are several ways to explore AI insights in Express List.

-   Quickly review if alerts have been processed by checking for the AI insights badge \[Omitted image "ai-insights-icon.png"\] Alt text:.
-   Search for specific information and key words in the Insights column. To add the column, see [Add or modify Express List columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/edit-list-columns-el.md) for more information.
-   Filter for information by using the **Insights** filter attribute in the filter panel.
-   Review **AI insights** in the preview panel or the alert record.

These options present differently, depending on whether the workflow is configured for automatic or manual execution.

-   When the workflow operates automatically, alerts are addressed as they’re created and AI insight information is displayed in Express List.
-   When the workflow operates manually, you must manually generate AI insights. For more information, see details in the following procedure.

For information about configuring this workflow, see [Configure the manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/configure-manage-alerts-autonomously-workflow.md).

## Procedure

1.  Navigate to **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the Express List icon \[Omitted image "express-list1.png"\].

3.  Review the AI insights through the following options.

<table id="choicetable_qzt_n1y_thc"><thead><tr><th align="left" id="d124257e276">

Review AI insights

</th><th align="left" id="d124257e279">

Procedure

</th></tr></thead><tbody><tr><td id="d124257e285">

**Check for the AI Insights badge for alert status**

</td><td>

-   If the AI insights icon \[Omitted image "ai-insights-icon.png"\] Alt text: is visible next to the check box, insights are available for that alert.
-   If insights aren't available for an alert, you can initiate the process manually. Details for generating insights are in the following options.


</td></tr><tr><td id="d124257e308">

**Search for alerts with AI Insights information and key words**

</td><td>

Search for content with the free text search. For more information, see [Find alert records in Express List using text search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/el-free-text-search.md).

</td></tr><tr><td id="d124257e324">

**Filter using AI Insights filter attribute**

</td><td>

Filter using the **Insights** attribute with a minimum string of two characters. For more information, see [Filtering the alert display in the Express List pane](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/filter-express-list.md).

</td></tr><tr><td id="d124257e343">

**Review AI insights in the preview panel**

</td><td>

1.  In the alerts list, select an alert by selecting the check box or the information icon \[Omitted image "info.png"\] Alt text: Information icon. next to the alert.
2.  -   In the **Insights** tab, review **AI insights**.
-   If data isn’t available for this alert, you can initiate the process by selecting **Generate**.


</td></tr><tr><td id="d124257e386">

**Review AI Insights in the alert record overview**

</td><td>

1.  In the alerts list, select an alert number to open the alert record.

The **Overview** tab is selected by default.

2.  -   If data is available, you can review the **AI insights** summary in the Summary section.
-   If data isn’t available for this alert, you can initiate the process by selecting **Generate**.


</td></tr></tbody>
</table>
**Parent Topic:**[Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md)

