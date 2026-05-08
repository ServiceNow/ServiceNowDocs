---
title: Using agentic workflow in Now Assist for Legal Service Delivery \(LSD\)
description: Use agentic workflows for Legal Service Delivery to analyze general legal requests, predict the appropriate legal category, and initiate a transfer after confirmation from the legal fulfiller or group manager.
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, AI Agents]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
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

For more information on the AI agents, see Now Assist AI agents.

To modify an agentic workflow, you must first duplicate it, and then update it. For more information, see:

-   Duplicate an agentic workflow
-   Create an agentic workflow
-   Modify an agentic workflow

**Note:**

-   When you modify an agentic workflow, AI agents, or tools, make sure that you update all instructions accordingly.
-   If you have a customized triage legal request agentic use case, update the script include of the business rule with the sys\_id of the customized use case. For more information, see [Activate the business rule for the Triage legal requests agentic workflow](../task/lsd-agentic-config-BR.md).

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

-   **[Triage legal requests agentic workflow](../task/trans-legal-request-agent.md)**  
Use the Triage legal requests agentic workflow to predict the appropriate legal category and to initiate a transfer after a confirmation from the legal fulfiller or group manager.

**Parent Topic:**[Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-landing.md)

