---
title: Use Now Assist for Zero Copy Connector agentic workflows and AI agents
description: Use Now Assist for Zero Copy Connector agentic workflows and AI agents to improve and enhance working with ERP data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist for Zero Copy Connector, Workflow Data Fabric]
---

# Use Now Assist for Zero Copy Connector agentic workflows and AI agents

Use Now Assist for Zero Copy Connector agentic workflows and AI agents to improve and enhance working with ERP data.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative and agentic AI in Now Assist for ZCC.

<table id="table_cxs_mpl_vfc"><thead><tr><th>

Agentic workflow

</th><th>

Description

</th><th>

Tools

</th></tr></thead><tbody><tr><td>

Explore ERP models

</td><td>

Answers questions about working with configured ERP database tables and models.

</td><td>

-   ERP action invoker AI agent
-   ERP data fetcher AI agent
-   ERP output formatter AI agent

</td></tr></tbody>
</table><table><thead><tr><th>

AI agent

</th><th>

Description

</th><th>

Tools

</th></tr></thead><tbody><tr><td>

OData Service Recommender

</td><td>

Identifies the most relevant OData service and endpoint, and can create a data model for the service if a model does not already exist.

</td><td>

-   Existing model checker
-   Model operation URL generator
-   Read endpoints
-   OData Service Checker
-   Model Creator
-   Use web search

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

## Role masking

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

## Standalone AI agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

