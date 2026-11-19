---
title: Configure the manage alerts autonomously agentic workflow
description: Configure an alert management rule to operate the manage alerts autonomously agentic workflow manually or automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/now-assist-for-it-operations-management/configure-manage-alerts-autonomously-workflow.html
release: yokohama
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-01-01"
reading_time_minutes: 4
breadcrumb: [Configuring agents and skills for ServiceNow Otto for ITOM, Configuring ServiceNow Otto for ITOM, ServiceNow Otto for ITOM, IT Operations Management]
---

# Configure the manage alerts autonomously agentic workflow

Configure an alert management rule to operate the manage alerts autonomously agentic workflow manually or automatically.

## Before you begin

-   [Install ServiceNow Otto for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md). For more information about installing Now Assist plugins, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/define-sec-controls-aw.md).

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator

## About this task

Configure the autonomous workflow alert management rule to operate the manage alerts autonomously agentic workflow manually or automatically. For more information about alert management rules, see [Alert management rules for resolving alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/alert-management-rule.md).

When the workflow operates automatically, alerts are addressed as they’re created and AI insight information is displayed in Express List.

When the workflow operates manually, users must manually generate AI insights. For more information, see [Review AI generated alert information and insights in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/now-assist-for-it-operations-management/use-ai-insights-express-list.md).

For more information about the manage alerts autonomously agentic workflow, see [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md).

**Note:**

If you change the alert management rule for the manage alert autonomously workﬂow, you must update the **sn\_aiops\_ai\_agents.autonomous\_alert\_rule\_sys\_id** property, which points to the alert management rule.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon \[Omitted image "icon-itom-aiops-config.png"\] Alt text: ITOM AIOps configuration center icon.

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the Optimize section, select **Respond to alerts**.

    The Respond page appears.

    \[Omitted image "respond-automation-page.png"\] Alt text: Respond automation page from where you can create automation to remediate action on alerts, escalate alerts or notify stakeholders.

4.  Select **Autonomous workflow** in the **Name** column.

    If the Edit automation pop-up is displayed, select **Open**. The Alert Management Rule form opens to the Alert info tab.

    **Note:** The **Active** check box is checked when the rule is enabled. To disable the rule and the manage alerts autonomously agentic workflow, remove the check by selecting the check box.

5.  Select the **Actions** tab to configure the execution information for the alert.

6.  In the **Execution** column, double-click the cell for the **Autonomous workflow**.

7.  Select the drop-down arrow to choose alert execution, and then select the green check mark to save. \[Omitted image "autonomous\_alert\_execution.png"\] Alt text: Execution information for the autonomous workflow alert management rule.


## What to do next

To learn more about generating AI insights with the manage alerts autonomously agentic workflow, see and [Review AI generated alert information and insights in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/now-assist-for-it-operations-management/use-ai-insights-express-list.md).

**Parent Topic:**[Configuring agents and skills for ServiceNow Otto for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/now-assist-for-it-operations-management/itom-ai-agent-configuration.md)

**Related topics**  


[Configure the Datadog analysis AI agent]()

[Configure the Dynatrace analysis AI agent]()

[Configure the Google Gemini Cloud Assist agent]()

[Configure the Kentik analysis AI agent]()

[Configure the New Relic analysis AI agent]()

