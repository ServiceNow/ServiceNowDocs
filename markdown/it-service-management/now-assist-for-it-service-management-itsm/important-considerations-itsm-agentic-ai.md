---
title: Important considerations for using Now Assist for IT Service Management \(ITSM\) agentic AI
description: Use the IT Service Management AI agents within an agentic workflow to complete tasks autonomously.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Important considerations for using Now Assist for IT Service Management \(ITSM\) agentic AI

Use the IT Service Management AI agents within an agentic workflow to complete tasks autonomously.

## Supported Large Language Models

**Note:**

-   You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

-   For the Now LLM Service updates, see [Now LLM Service updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/now-llm-model-updates.md).

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user.For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md)

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

## Considerations for running the autonomous AI Agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.
-   Azure OpenAI is recommended for ITSM agentic workflows. For information on Large Language Models \(LLMs\) for AI agents and agentic workflows, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

## Standalone AI agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

