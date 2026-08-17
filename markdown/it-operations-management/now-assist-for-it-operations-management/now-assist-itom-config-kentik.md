---
title: Configure the Kentik analysis AI agent
description: Configure the Kentik analysis AI agent for the analyze alert impact agentic workflow. This configuration also supports the Kentik observability skill in the manage alerts autonomously agentic workflow. After you configure the agent, the workflows can surface information from Kentik to help you investigate alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-config-kentik.html
release: yokohama
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring agents and skills for ServiceNow Otto for ITOM, Configuring ServiceNow Otto for ITOM, ServiceNow Otto for ITOM, IT Operations Management]
---

# Configure the Kentik analysis AI agent

Configure the Kentik analysis AI agent for the analyze alert impact agentic workflow. This configuration also supports the Kentik observability skill in the manage alerts autonomously agentic workflow.After you configure the agent, theworkflows can surface information from Kentik to help you investigate alerts.

## Before you begin

Before configuring the Kentik analysis AI agent, you must do the following:

-   [Install ServiceNow Otto for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
-   [Integrate Kentik alerts with Event Management](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2113973).
-   Copy your Kentik connection URL, API token, and the email address associated with the API token.

    The Kentik API token requires this permission: Can view devices.


Role required: connection\_admin and credential\_admin

## Procedure

1.  Navigate to **All** &gt; **sys\_alias.LIST**.

2.  Search for and select **Kentik analysis AI agent**.

3.  Select **Create New Connection &amp; Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Connection Name**|Name of your Kentik connection. This name helps you identify it later. For example, Kentik Prod.|
    |**Connection URL**|URL of your Kentik instance. Kentik URLs follow this format: `https://<your-resource-name>.api.kentik.com`.|
    |**User Email**|Email address associated with the Kentik API token.|
    |**API Token**|Kentik API token.|

5.  Select **Create**.

    Your connection appears in the **Connections** tab.


## What to do next

Activate the Kentik analysis AI agent to use it in the analyze alert impact agentic workflowor manage alerts autonomously agentic workflow. In AI Agent Studio, navigate to **Create and manage**, find the Kentik analysis AI agent, and turn on the agent in the Select channels and status screen.

**Note:** To use the Kentik analysis AI agent in the analyze alert impact agentic workflow, make sure that the Alert impact summary and Alert information retrieval AI agents are active. They're also required for the analyze alert impact agentic workflow.

To learn more about using the Kentik analysis AI agent in the analyze alert impact agentic workflowor manage alerts autonomously agentic workflow, see [Use the analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-use-aia.md)and [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/now-assist-for-it-operations-management/itom-autonomous-operator-workflow.md).

**Parent Topic:**[Configuring agents and skills for ServiceNow Otto for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/now-assist-for-it-operations-management/itom-ai-agent-configuration.md)

**Related topics**  


[Configure the Datadog analysis AI agent]()

[Configure the Dynatrace analysis AI agent]()

[Configure the Google Gemini Cloud Assist agent]()

[Configure the New Relic analysis AI agent]()

[Configure the manage alerts autonomously agentic workflow]()

