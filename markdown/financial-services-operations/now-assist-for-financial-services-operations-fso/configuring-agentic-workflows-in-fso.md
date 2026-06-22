---
title: Configure agentic workflows in Financial Services Operations
description: Activate and modify agentic workflows for Now Assist for FSO in AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-agentic-workflows-in-fso.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configuring fso agentic workflows, configuring fso ai agents]
breadcrumb: [Configure, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configure agentic workflows in Financial Services Operations

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

To modify an agentic workflow, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate the agent within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

For more information on activating agentic workflows, triggers, and agents, see [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/activate-aia-use-case.md) and [Modify an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/modify-ai-agent.md).

For more information on agentic workflows in FSO, see [Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/using-ai-agent-use-cases-in-now-assist-for-fso.md).

## Choosing a language model service provider

You can choose which service provider to use for AI agents and agentic workflows [in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/edit-model-providers.md).

**Parent Topic:**[Configuring Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-now-assist-skills-for-fso.md)

