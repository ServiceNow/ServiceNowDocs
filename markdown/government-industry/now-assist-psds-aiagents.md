---
title: Standalone AI Agents in Public Sector Digital Services
description: Use standalone agents to achieve specific automated outcomes with the Public Sector Digital Services AI Agent Collection application. ​
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use agentic AI, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Standalone AI Agents in Public Sector Digital Services

Use standalone agents to achieve specific automated outcomes with the Public Sector Digital Services AI Agent Collection application. ​

**Important:** In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

The following table describes the available AI agents in the Now Assist for Public Sector Digital Services \(PSDS\) application.

<table id="table_hzb_sd4_cfc"><thead><tr><th>

AI Agent name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Information Request Playbook Fee Estimation Agent

</td><td>

-   Analyzes fee waiver justification from applicant for an information request case record, and validates justification against predefined rules
-   Outlines the steps required to estimate the fees associated with an information request
-   Retrieves similar case records and allows user to exclude any from the fee calculation
-   Estimates and communicates fee breakdown associated with an information request case record based on similar request queries and request details from the user
-   Communicates sub-total estimate, fee waiver recommendation, and total with fee waiver.

</td></tr></tbody>
</table>**Note:** Verify that AI Search is enabled on the instance before configuring the agents.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see Implement access control in Now Assist AI agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.
-   Azure OpenAI is recommended for ITSM agentic workflows. For information on Large Language Models \(LLMs\) for AI agents and agentic workflows, see Select the LLM for AI agents and agentic workflows.

For more information on configuring AI Agents, see [Activate an AI Agent in Public Sector Digital Services AI Agent Collection](psds-config-activate-ai-agents.md).

