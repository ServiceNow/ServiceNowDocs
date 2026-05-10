---
title: Using agentic AI for Operational Technology Service Management
description: Use the Operational Technology Service Management \(OTSM\) AI agent collection to complete tasks autonomously.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist for OTSM, Operational Technology]
---

# Using agentic AI for Operational Technology Service Management

Use the Operational Technology Service Management \(OTSM\) AI agent collection to complete tasks autonomously.

|Agentic workflow name|Description|Available AI agents|
|---------------------|-----------|-------------------|
|Generate OT KB articles|Upon OT Incident resolution, the AI agent automatically creates a KB article with relevant contextual information.|OT knowledge generator AI agent|

**Important:** If you want to change this agentic workflow, you can [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

The minimum role needed to duplicate an agentic workflow is the **sn\_aia.admin** role. By default, the OTSM agentic workflow is inactive. If you want to use the OOB agentic workflow, you can activate the OOB trigger. But if you want to customize the agentic workflow, you must duplicate it.

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

## Supported Large Language Models

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md)

## Considerations for running the autonomous AI agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.

## Standalone AI agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

## Role masking

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

