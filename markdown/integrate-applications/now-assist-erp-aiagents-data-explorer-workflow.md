---
title: Explore ERP models agentic workflow
description: Use the Explore ERP models AI agent team in Now Assist for Zero Copy Connector to obtain information about working with ERP database tables and models.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use agentic AI, Now Assist for Zero Copy Connector, Workflow Data Fabric]
---

# Explore ERP models agentic workflow

Use the Explore ERP models AI agent team in Now Assist for Zero Copy Connector to obtain information about working with ERP database tables and models.

## Explore ERP models agentic workflow overview

The Explore ERP models agentic workflow uses a team of AI agents to answer user questions about working with ERP database tables and identifying models configured in ERP content packs.

## Prerequisites for the Explore ERP models agentic workflow

-   The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in Now Assist for ZCC.
-   You must have the Knowledge Graph plugin installed. For more information, see [Configuring Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/configuring-knowledge-graph.md).
-   Follow the steps in [Now Assist for Zero Copy Connector agentic workflow prerequisites](now-assist-erp-ai-agents-prereqs.md) before using the Explore ERP models agentic workflow.

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

    ![Explore ERP models page with information about the workflow and the AI agents in the workflow.](../images/erp-data-product-explorer-workflow-listing.png)

3.  Review the **Workflow description** and **List of steps**.
4.  Review the **Add AI agents that can perform these steps** section and select an AI agent name for details. For more information, see [Define key requirements for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-key-requirements.md).
5.  Select **Save and continue** and view the user access options. For more information, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).
6.  Select **Save and continue** and view the data access options. For more information, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).
7.  Select **Save and continue** and view the trigger options. For more information, see [Add a trigger to an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aw.md).
8.  Select **Save and continue** and view the channel and status options. For more information, see [Select channels and access for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/channels-access-aw.md).
9.  Select **Save and test** to test the workflow. For more information, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

## Using the Explore ERP models agentic workflow

In this example, use the Explore ERP models agentic workflow to run a specific model.

1.  Select the Now Assist icon \(![](../images/now-assist-sparkle-icon-dark.png)\) from anywhere in your instance to open the Now Assist panel.
2.  Ask for information in plain language. For example, `I want to run the Order Details model`.

    ![Now Assist panel with question typed in.](../images/erp-data-explorer-workflow7.png)

3.  Select the **Explore ERP models** option.

    ![Now Assist panel with explore ERP models option highlighted.](../images/erp-data-explorer-workflow8.png)

4.  Select **Go to the ERP Model**.

    ![Now Assist panel with go to the erp model option highlighted.](../images/erp-data-explorer-workflow9.png)

5.  If there are mandatory fields, provide the correct information in the specified format. You have the option to also include additional fields.

    Now Assist provides the information you requested.

    ![Now Assist panel with order details listed.](../images/erp-data-explorer-workflow11.png)


Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(![New chat icon.](../../../common/image/icon-zoom-in.png)\).

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

