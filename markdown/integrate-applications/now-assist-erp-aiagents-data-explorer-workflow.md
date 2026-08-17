---
title: Explore ERP models agentic workflow
description: Use the Explore ERP models AI agent team in ServiceNow Otto for Zero Copy Connector to obtain information about working with ERP database tables and models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/now-assist-erp-aiagents-data-explorer-workflow.html
release: australia
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use agentic AI, ServiceNow Otto for Zero Copy Connector, Workflow Data Fabric]
---

# Explore ERP models agentic workflow

Use the Explore ERP models AI agent team in ServiceNow Otto for Zero Copy Connector to obtain information about working with ERP database tables and models.

## Explore ERP models agentic workflow overview

The Explore ERP models agentic workflow uses a team of AI agents to answer user questions about working with ERP database tables and identifying models configured in ERP content packs.

## Prerequisites for the Explore ERP models agentic workflow

-   The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in ServiceNow Otto for ZCC.
-   You must have the Knowledge Graph plugin installed. For more information, see [Configuring Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-knowledge-graph.md).
-   Follow the steps in [ServiceNow Otto for Zero Copy Connector agentic workflow prerequisites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-erp-ai-agents-prereqs.md) before using the Explore ERP models agentic workflow.

## AI agents used in the Explore ERP models agentic workflow

The following agents are used in the Explore ERP models agentic workflow.

|AI agent|AI agent role|
|--------|-------------|
|ERP action invoker AI agent|Gathers information for a specific operation and generates mandatory and optional inputs. Users can fill in a form to provide values for the mandatory inputs. The AI agent then formats and sends the inputs to an action script that creates the operation.|
|ERP data fetcher AI agent|Retrieves information about relevant models and model operations. Currently supports Read operations.|
|ERP output formatter AI agent|Refines and formats the information from the ERP action invoker AI agent.|

## Using the Explore ERP models agentic workflow

In this example, use the Explore ERP models agentic workflow to run a specific model.

1.  Select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance to open the Otto panel.
2.  Ask for information in plain language. For example, `I want to run the Order Details model`.
3.  Select the **Explore ERP models** option.
4.  Select **Go to the ERP Model**.
5.  If there are mandatory fields, provide the correct information in the specified format. You have the option to include additional fields.

    Otto provides the information you requested.


Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(\[Omitted image "icon-zoom-in.png"\]\).

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

