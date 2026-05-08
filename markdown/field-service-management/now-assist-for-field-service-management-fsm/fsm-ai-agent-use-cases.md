---
title: Using agentic AI in Now Assist for Field Service Management \(FSM\)
description: Use the AI agent collection for Field Service Management to create work orders and manage parts on the platform or the ServiceNow Agent application.
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 2
keywords: [Generative AI, generative AI for Field Service Management, AI agent, Parts Manager]
breadcrumb: [Now Assist for FSM]
---

# Using agentic AI in Now Assist for Field Service Management \(FSM\)

Use the AI agent collection for Field Service Management to create work orders and manage parts on the platform or the ServiceNow Agent application.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

|AI agents|Description|
|---------|-----------|
|Create work order|Creates a work order using text or an image. The AI agent can be accessed on the platform or on the ServiceNow Agent mobile application.|
|Parts Manager|Tracks and validates parts usage when closing work order tasks. The AI agent analyzes activity notes to update parts statuses and automatically adjusts inventory. The AI agent can be accessed on the platform or on the ServiceNow Agent mobile application.|

To install and set up AI agents on your instance, see Install Now Assist AI agents and Set up Now Assist AI agents.

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see Implement access control in Now Assist AI agents.

**Important:** By default, all agentic workflows and AI agent records are read only.

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

