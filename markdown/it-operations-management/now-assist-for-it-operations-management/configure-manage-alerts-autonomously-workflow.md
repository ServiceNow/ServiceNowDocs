---
title: Configure the manage alerts autonomously agentic workflow
description: Configure an alert management rule to operate the manage alerts autonomously agentic workflow manually or automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/now-assist-for-it-operations-management/configure-manage-alerts-autonomously-workflow.html
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for ITOM, IT Operations Management]
---

# Configure the manage alerts autonomously agentic workflow

Configure an alert management rule to operate the manage alerts autonomously agentic workflow manually or automatically.

## Before you begin

-   [Install Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md). For more information about installing Now Assist plugins, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md).
-   \[Optional\] Additional configuration is required for some skills used in the agentic workflow:
    -   **Observability skills**: Configure the relevant observability skills to surface data from observability tools integrated with Event Management. See [Configure observability agents for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md).
    -   **Log analytics skills**: Install and configure Health Log Analytics to enable analysis of log analytics alerts. See [Configuring Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-configuring.md).

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator

## About this task

Configure the autonomous workflow alert management rule to operate the manage alerts autonomously agentic workflow manually or automatically. For more information about alert management rules, see [Alert management rules for resolving alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-management-rule.md).

When the workflow operates automatically, alerts are addressed as they’re created and AI insight information is displayed in Express List.

When the workflow operates manually, users must manually generate AI insights. For more information, see [Review AI generated alert information and insights in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/use-ai-insights-express-list.md).

For more information about the manage alerts autonomously agentic workflow, see [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md).

**Note:**

If you change the alert management rule for the manage alert autonomously workﬂow, you must update the **sn\_aiops\_ai\_agents.autonomous\_alert\_rule\_sys\_id** property, which points to the alert management rule.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon \[Omitted image "icon-itom-aiops-config.png"\] Alt text: ITOM AIOps configuration center icon.

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the Optimize section, select **Respond to alerts**.

    The Respond page appears.

    \[Omitted image "respond-automation-page.png"\] Alt text: Respond automation page from where you can create automation to remediate action on alerts, escalate alerts or notify stakeholders.

4.  In the Name column, select **Autonomous workflow**.

    If the Edit automation pop-up is displayed, select **Open**. The Alert Management Rule form opens to the Alert info tab.

    **Note:** The **Active** check box is selected when the rule is enabled. To disable the rule and the manage alerts autonomously agentic workflow, select the check box.

5.  Configure the execution information for the alert by selecting the **Actions** tab.

6.  In the Execution column, double-click the cell for the **Autonomous workflow**.

7.  Select the drop-down arrow to choose alert execution, and then select the green check mark to save. \[Omitted image "autonomous\_alert\_execution.png"\] Alt text: Execution information for the autonomous workflow alert management rule.


## What to do next

To learn more about generating AI insights with the manage alerts autonomously agentic workflow, see [Review AI generated alert information and insights in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/use-ai-insights-express-list.md).

-   **[Configure the Dynatrace analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-config-dynatrace.md)**  
Configure the Dynatrace analysis AI agent for the analyze alert impact agentic workflow. This configuration also supports the Dynatrace observability skill in the manage alerts autonomously agentic workflow.After you configure the agent, the workflows can surface information from Dynatrace to help you investigate alerts.
-   **[Configure the Google Gemini Cloud Assist agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-config-google-cloud.md)**  
Configure the Google Gemini Cloud Assist agent to use the Gemini Cloud Assistant observability skill in the manage alerts autonomously agentic workflow. Once configured, the skill gathers information to help you investigate alerts.

**Parent Topic:**[Configure Now Assist for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-configure.md)

