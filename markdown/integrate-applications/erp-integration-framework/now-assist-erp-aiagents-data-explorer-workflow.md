---
title: Explore ERP models agentic workflow
description: Use the Explore ERP models AI agent team in Now Assist for Zero Copy Connector to obtain information about working with ERP database tables and models.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Now Assist, Agentic AI, generative AI, Gen AI, zero copy connector, erp]
breadcrumb: [Use agentic workflows in Now Assist for Zero Copy Connector, Now Assist for Zero Copy Connector, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Explore ERP models agentic workflow

Use the Explore ERP models AI agent team in Now Assist for Zero Copy Connector to obtain information about working with ERP database tables and models.

## Explore ERP models agentic workflow overview

This feature is available starting with the Zurich Patch 4 release.

The Explore ERP models agentic workflow uses a team of AI agents to answer user questions about working with ERP database tables and identifying models configured in ERP data products.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in Now Assist for Zero Copy Connector.

## Prerequisites and setup

You must have the Knowledge Graph plugin installed. For more information, see [Configuring Knowledge Graph](https://www.servicenow.com/docs/access?context=configuring-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Role masking

Required role: sn\_erp\_integration.erp\_admin.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Check status of assistants

Now Assist in Virtual Agent and Now Assist panel must be on. For information about how to check the status of assistants, see [Manage LLM virtual agents on the Assistants screen](https://www.servicenow.com/docs/access?context=manage-llm-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

## Activate conversational skills

In Now Assist in Virtual Agent, check that **Now Assist Q&amp;A**, **Now Assist Topics**, and **AI agents** are activated.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.
2.  Select an assistant such as Now Assist in Virtual Agent \(default\).
3.  Select **Now Assist skills** in left side menu.
4.  Ensure that **Now Assist Q&amp;A**, **Now Assist Topics**, and **AI agents** are activated. Activate if necessary.

## Set large language model \(LLM\) provider and check connection

Set a large language model \(LLM\) provider and have a least one connection. For more information about available providers and setting a provider, see [Manage AI models](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

1.  To check for an active connection, navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.
2.  Select an alias, for example, **Azure OpenAI**.
3.  Select the **Connections** tab.
4.  At least one connection should be listed with **Active** set to **true**.

    ![Azure OpenAI connection and credential alias record with connections tab displayed showing one active connection.](../image/erp-data-explorer-workflow4.png)

    **Note:** For more information about creating a connection and making it active, see [Get started with connections](https://www.servicenow.com/docs/access?context=connection-information&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).


## AI agents used in the Explore ERP models agentic workflow

The following agents are used in the Explore ERP models agentic workflow.

|AI agent|AI agent role|
|--------|-------------|
|ERP action invoker AI agent|Gathers information for a specific operation and generates mandatory and optional inputs. Users can fill in a form to provide values for the mandatory inputs. The AI agent then formats and sends the inputs to an action script that creates the operation.|
|ERP data fetcher AI agent|Retrieves information about relevant models and model operations. Currently supports Read operations.|
|ERP output formatter AI agent|Refines and formats the information from the ERP action invoker AI agent.|

## Accessing the Explore ERP models agentic workflow

Users with the sn\_aia\_admin role can access the workflow.

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Explore ERP models**.

    ![ERP Data Product Explorer page with information about the workflow and the AI agents in the workflow.](../image/erp-data-product-explorer-workflow-listing.png)

3.  Review the **Workflow description** and **List of steps**.
4.  Review the **Add AI agents that can perform these steps** section and select an AI agent name for details. For more information, see [Define key requirements for an agentic workflow](https://www.servicenow.com/docs/access?context=define-key-requirements&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
5.  Select **Save and continue** and view the user access options. For more information, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
6.  Select **Save and continue** and view the data access options. For more information, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
7.  Select **Save and continue** and view the trigger options. For more information, see [Add a trigger to an agentic workflow](https://www.servicenow.com/docs/access?context=add-trigger-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
8.  Select **Save and continue** and view the channel and status options. For more information, see [Select channels and access for an agentic workflow](https://www.servicenow.com/docs/access?context=channels-access-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
9.  Select **Save and test** to test the workflow. For more information, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Using the Explore ERP models agentic workflow

Select the Now Assist icon \(![](../image/now-assist-sparkle-icon-dark.png)\) from anywhere in your instance to open the Now Assist panel.

Ask for information in plain language. For example, `I want to run the Order Details model`.

![Now Assist panel with question typed in.](../image/erp-data-explorer-workflow7.png)

Select the **Explore ERP models** option.

![Now Assist panel with explore ERP models option highlighted.](../image/erp-data-explorer-workflow8.png)

Select **Go to the ERP Model**.

![Now Assist panel with go to the erp model option highlighted.](../image/erp-data-explorer-workflow9.png)

If there are mandatory fields, provide the correct information in the specified format. You have the option to also include additional fields.

Now Assist provides the information you requested.

![Now assist panel with answer to question displayed.](../image/erp-data-explorer-workflow11.png)

Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(![New chat icon.](../../../common/image/icon-zoom-in.png)\).

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

