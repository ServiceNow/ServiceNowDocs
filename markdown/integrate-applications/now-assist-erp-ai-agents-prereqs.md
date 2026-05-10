---
title: Now Assist for Zero Copy Connector agentic workflow prerequisites
description: Before you use Now Assist for Zero Copy Connector agentic workflows, you must complete several prerequisites.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-24"
reading_time_minutes: 1
breadcrumb: [Use agentic AI, Now Assist for Zero Copy Connector, Workflow Data Fabric]
---

# Now Assist for Zero Copy Connector agentic workflow prerequisites

Before you use Now Assist for Zero Copy Connector agentic workflows, you must complete several prerequisites.

## Role masking

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

## Check status of assistants

Now Assist in Virtual Agent and Now Assist panel must be on. For information about how to check the status of assistants, see [Manage LLM virtual agents on the Assistants screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/manage-llm-va.md)

## Activate conversational skills

In Now Assist in Virtual Agent, check that **Now Assist Q&amp;A**, **Now Assist Topics**, and **AI agents** are activated.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.
2.  Select **Manage assistants**.
3.  Select Now Assist in Virtual Agent.
4.  Select **Now Assist skills** in the left side menu.
5.  Confirm that **Now Assist Q&amp;A**, **Now Assist Topics**, and **AI agents** are activated. Activate if necessary.

## Set large language model \(LLM\) provider and check connection

Set a large language model \(LLM\) provider and have at least one connection. For more information about available providers and setting a provider, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

1.  To check for an active connection, navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.
2.  Select an alias, for example, **Azure OpenAI**.
3.  Select the **Connections** tab.
4.  At least one connection should be listed with **Active** set to **true**.

    ![Azure OpenAI connection and credential alias record with connections tab displayed showing one active connection.](../images/erp-data-explorer-workflow4.png)

    **Note:** For more information about creating a connection and making it active, see [Get started with connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-information.md).


