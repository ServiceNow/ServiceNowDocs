---
title: Using agentic workflow in Now Assist for Legal Service Delivery \(LSD\)
description: Use agentic workflows for Legal Service Delivery to analyze general legal requests, predict the appropriate legal category, and initiate a transfer after confirmation from the legal fulfiller or group manager.
locale: en-US
release: yokohama
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, AI Agents]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Using agentic workflow in Now Assist for Legal Service Delivery \(LSD\)

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

-   Record field value prediction AI agent
-   Transfer legal request AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

For more information on the AI agents, see [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

To modify an agentic workflow, you must first duplicate it, and then update it. For more information, see:

-   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
-   [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
-   [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

**Note:**

-   When you modify an agentic workflow, AI agents, or tools, make sure that you update all instructions accordingly.
-   If you have a customized triage legal request agentic use case, update the script include of the business rule with the sys\_id of the customized use case. For more information, see [Activate the business rule for the Triage legal requests agentic workflow](../task/lsd-agentic-config-BR.md).

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

-   **[Configuring the Triage legal requests agentic workflow](../task/conf-transfer-legal-request-agent.md)**  
You can configure the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer when a legal fulfiller or group manager confirms the request.
-   **[Triage legal requests agentic workflow](../task/trans-legal-request-agent.md)**  
Use the Triage legal requests agentic workflow to predict the appropriate legal category and to initiate a transfer after a confirmation from the legal fulfiller or group manager.

**Parent Topic:**[Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-landing.md)

