---
title: Enable AI capabilities in Financial Services Operations
description: Plan and configure your implementation of AI skills and agents in Financial Services Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/enable-ai-capabilities-in-fso.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 2
breadcrumb: [Configure, Financial Services Operations \(FSO\)]
---

# Enable AI capabilities in Financial Services Operations

Plan and configure your implementation of AI skills and agents in Financial Services Operations.

## Choosing a language model service provider

Different models can provide different performance and responses. You can choose which service provider to use for your ServiceNow Otto skills and agentic AI.

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

When activating a new or inactive FSO skill, Anthropic Claude on AWS is set as the default model provider.

**Note:** See [Federal exclusion notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/exploring-now-assist-for-financial-services-operations-fso.md) for more information.

## Configuring ACLs

You can enable security implementation on AI skills, AI agents, and agentic workflows through access control lists \(ACLs\) and user identities. These ACLs determine which users have permissions to discover and invoke these features.

Configure and manage ACLs for agentic workflows and AI agents in the AI Agent Studio. See [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md) for more details.

Predefined ACLs exist for the following:

-   Case summarization skills
-   Disputes intake via Virtual Agent
-   AI agents and agentic workflows in Help Resolve Friendly Fraud
-   Subflows used in Disputes intake via Virtual Agent
-   Subflows and subflow actions used in the Help Resolve Friendly Fraud agentic workflow

See [Configure an ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_CreateAnACLRule.md) for more information on configuring ACLs.

## Role masking

Required roles: sn\_bom\_credit\_card.dispute\_agent, sn\_bom\_credit\_card.dispute\_agent\_connector.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to any activated FSO AI agents.

**Related topics**  


[Configure Financial Services Operations AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-fso-now-assist-skills.md)

[Configure agentic workflows in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configuring-agentic-workflows-in-fso.md)

[Configure Financial Services Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-fso-ai-agents.md)

[Skill inputs for ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/skill-inputs-and-triggers-for-now-assist-for-financial-services-operations-fso.md)

