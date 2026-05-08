---
title: Use agentic AI in Now Assist for Public Sector Digital Services \(PSDS\)
description: Use standalone agents to achieve specific automated outcomes with the Public Sector Digital Services AI Agent Collection application. ​
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Use agentic AI in Now Assist for Public Sector Digital Services \(PSDS\)

Use standalone agents to achieve specific automated outcomes with the Public Sector Digital Services AI Agent Collection application. ​

AI Agents are configurable through the AI Agent Studio. The AI Agent Studio is available to administrators as part of the Now Assist for Public Sector Digital Services \(PSDS\) offering. The AI Agent Studio allows admins to configure, test, and manage AI agents using natural language and prebuilt workflows. These agents can automate tasks like fee estimation and information request handling.

This table describes the use cases in Now Assist for Public Sector Digital Services \(PSDS\).

|Use case|Description|
|--------|-----------|
|Estimate fee breakdown for an information request|Helps government service agents determine the fee breakdown for an information request by working to arrive at a subtotal fee estimate, a recommendation for whether a fee waiver request should be approved or rejected, including reasons for any rejection, and a total fee estimate, with the fee waiver, if applicable.|

Find information such as the Large Language Models \(LLM\) supported in Now Assist and security controls that are important considerations for using agentic AI.

## Supported Large Language Models

**Note:**

-   You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

-   For the Now LLM Service updates, see Now LLM Service updates.

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user.For more information, see Implement access control in Now Assist AI agents

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an AI agent.

## Considerations for running the autonomous AI Agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.
-   Azure OpenAI is recommended for ITSM agentic workflows. For information on Large Language Models \(LLMs\) for AI agents and agentic workflows, see Large language models on the ServiceNow AI Platform®.

## Standalone AI agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

For information on the standalone Public Sector Digital Services AI agents, see [Standalone AI Agents in Public Sector Digital Services](now-assist-psds-aiagents.md).

