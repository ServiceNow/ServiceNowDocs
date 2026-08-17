---
title: Configure agentic workflows in Financial Services Operations
description: Agentic workflows in FSO automate dispute resolution tasks by orchestrating AI agents that analyze transactions and generate recommendations. Activate workflows in AI Agent Studio to enable automated assistance for human agents handling friendly fraud cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/configuring-agentic-workflows-in-fso.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [configuring fso agentic workflows, configuring fso ai agents]
breadcrumb: [Enable AI capabilities, Configure, Financial Services Operations \(FSO\)]
---

# Configure agentic workflows in Financial Services Operations

Agentic workflows in FSO automate dispute resolution tasks by orchestrating AI agents that analyze transactions and generate recommendations. Activate workflows in AI Agent Studio to enable automated assistance for human agents handling friendly fraud cases.

The following table shows the available agentic workflows in FSO:

<table id="table_ftm_yyr_t2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help resolve friendly fraud disputes

</td><td>

Assists human dispute agents with handling transactions flagged as friendly fraud. It leverages the results from a friendly fraud detection tool to generate recommendations for the appropriate action. If the transaction is rejected, the AI agent also helps draft an explanation for the end user.

</td><td>

Friendly fraud AI agent

</td></tr></tbody>
</table>## Activating agentic workflows

Agentic workflows in FSO are inactive by default. To activate a workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select the agentic workflow.
3.  In the guided setup, select **Define trigger**.
4.  Select the agentic workflow trigger in the list.
5.  In the Edit trigger form, set **Active** to true.
6.  Select **Save**.

## Modifying agentic workflows

**Important:** By default, all agentic workflows and AI agent records are read only.

To modify an agentic workflow, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate the agent within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

For more information on activating agentic workflows, triggers, and agents, see [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md) and [Modify an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-ai-agent.md).

## Choosing a language model service provider

You can choose which service provider to use for AI agents and agentic workflows in the AI Admin Hub console. For more information, see [Manage model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/edit-model-providers.md).

**Related topics**  


[Help resolve friendly fraud disputes agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/friendly-fraud-agentic-ai-workflow.md)

[Detect friendly fraud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resolve-friendly-fraud.md)

