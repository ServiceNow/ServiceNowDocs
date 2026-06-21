---
title: Configuring agentic workflows in Financial Services Operations
description: Activate and modify agentic workflows for Now Assist for FSO in AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-agentic-workflows-in-fso.html
release: yokohama
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-04-17"
reading_time_minutes: 1
keywords: [configuring fso agentic workflows, configuring fso ai agents]
breadcrumb: [Configuring Now Assist for FSO, Now Assist for Financial Services Operations \(FSO\)]
---

# Configuring agentic workflows in Financial Services Operations

Activate and modify agentic workflows for Now Assist for FSO in AI Agent Studio.

## Activating agentic workflows

Agentic workflows in FSO are inactive by default. To activate a workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select the agentic workflow.
3.  In the guided setup, select **Define trigger**.
4.  Select the agentic workflow trigger in the list.
5.  In the Edit trigger form, set **Active** to true.
6.  Select **Save**.

## Modifying agentic workflows

**Important:** By default, all agentic workflows and AI agent records are read only.

To modify an agentic workflow, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate the agent within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

For more information on activating agentic workflows, triggers, and agents, see  and .

For more information on agentic workflows in FSO, see [Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/using-ai-agent-use-cases-in-now-assist-for-fso.md).

## Choosing a language model service provider

You can choose which service provider to use for AI agents and agentic workflows in the Now Assist Admin console.

## Role masking

Required roles: sn\_bom\_credit\_card.dispute\_agent, sn\_bom\_credit\_card.dispute\_agent\_connector.

Role masking enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

In the data access settings, you must also add the necessary roles to Resolve friendly fraud using Agentic AI.

