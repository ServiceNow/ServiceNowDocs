---
title: Using agentic workflows in Now Assist for Legal Service Delivery \(LSD\)
description: Use agentic workflows for Legal Service Delivery to analyze general legal requests, predict the appropriate legal category, and initiate a transfer after confirmation from the legal fulfiller or group manager.
locale: en-US
release: xanadu
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2025-04-09"
reading_time_minutes: 1
keywords: [Now Assist, generative AI, AI Agents]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Using agentic workflows in Now Assist for Legal Service Delivery \(LSD\)

Use agentic workflows for Legal Service Delivery to analyze general legal requests, predict the appropriate legal category, and initiate a transfer after confirmation from the legal fulfiller or group manager.

<table id="table_bqn_lt4_x2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Triage legal requests

</td><td>

Uses AI agents to analyze general legal requests, predict the appropriate legal category, and initiate a transfer upon a confirmation from the legal fulfiller. The agentic workflow enhances response times, reduces manual tasks, and improves overall productivity.**Note:** The agentic workflow is triggered in the Now Assist panel. It is not supported in the Virtual Agent panel.

</td><td>

-   Record management AI agent
-   Record field value prediction AI agent
-   Transfer legal request AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

For more information about the AI agents, see [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

To run the AI agents autonomously, you must first [duplicate the use case](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and then proceed with the following steps:

-   Activate the agentic workflow. For more information, see [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   Activate all agents within the workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

**Note:**

-   When you modify an agentic workflow, AI agents, or tools, make sure that you update all instructions accordingly.
-   If you have a customized triage legal request agentic use case, update the script include of the business rule with the sys\_id of the customized use case. For more information, see [Activate the business rule for the Triage legal requests agentic workflow](../task/lsd-agentic-config-BR.md).

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

