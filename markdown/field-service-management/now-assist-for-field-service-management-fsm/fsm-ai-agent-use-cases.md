---
title: Using agentic AI in Now Assist for Field Service Management \(FSM\)
description: Use the AI agent collection for Field Service Management to create work orders and manage parts on the platform or the ServiceNow Agent application.
locale: en-US
release: zurich
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2026-02-23"
reading_time_minutes: 2
keywords: [Generative AI, generative AI for Field Service Management, AI agent, Parts Manager]
breadcrumb: [Now Assist for FSM]
---

# Using agentic AI in Now Assist for Field Service Management \(FSM\)

Use the AI agent collection for Field Service Management to create work orders and manage parts on the platform or the ServiceNow Agent application.

|AI agents|Description|
|---------|-----------|
|Create work order|Creates a work order using text or an image. The AI agent can be accessed on the platform or on the ServiceNow Agent mobile application.|
|Parts Manager|Tracks and validates parts usage when closing work order tasks. Field technicians use conversational AI to swap, install, or decline required parts. The AI agent can be accessed on the platform or on the ServiceNow Agent mobile application.|

To install and set up AI agents on your instance, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Set up Now Assist AI agents](https://www.servicenow.com/docs/access?context=set-up-na-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Important:** By default, all agentic workflows and AI agent records are read only.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

