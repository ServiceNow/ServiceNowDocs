---
title: AI Service Graph connector for LangGraph
description: Use the  AI Service Graph Connector for LangGraph to create AI connections to discover and imports AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets from LangGraph into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph connector for LangGraph

Use the  AI Service Graph Connector for LangGraph to create AI connections to discover and imports AI assets such as AI systems, agents, models, prompts, tools, and datasets as well as usage data for these AI assets from LangGraph into AI Control Tower. This usage information is consumed by the AI Control Tower's value dashboard.

## Download apps from the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home)  website to download the AI Service Graph Connector for LangGraph app.

## Supported ServiceNow versions

-   Australia
-   Zurich patch 7
-   Yokohama patch 11

## User roles

Roles required in the ServiceNow environment:

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Prerequisites from LangGraph

Enter the connection details, API Key credentials and update the credential record.

Create an API key for the AI Connector to authenticate with LangGraph. For more information on creating API Key in LangGraph, see [Create an API Key](../task/create-an-api-key-in-langgraph-environment.md)

**Note:** To access the latest and most comprehensive guidelines for managing API keys, see [About LangGraph](https://docs.langchain.com/)

## Data Mapping

The following table lists the data sources, the staging tables, and the target tables  CMDB CI classes and non-CMDB  classes where data is stored for LangGraph project.

<table id="table_s1w_52q_m3c"><tbody><tr><td>

Data Source

</td><td>

Import Set Table

</td><td>

Target Table\(s\)

</td></tr><tr><td>

SG-LangGraph Agents

</td><td>

sn\_langgraph\_integ\_agents

</td><td>

alm\_ai\_system\_digital\_asset

 alm\_ai\_prompt\_digital\_asset

 cmdb\_ci\_function\_ai

</td></tr><tr><td>

SG-LangGraph Usage

</td><td>

sn\_langgraph\_integ\_usage

</td><td>

alm\_ai\_model\_digital\_asset

 sn\_ai\_disc\_ai\_usage

</td></tr></tbody>
</table>