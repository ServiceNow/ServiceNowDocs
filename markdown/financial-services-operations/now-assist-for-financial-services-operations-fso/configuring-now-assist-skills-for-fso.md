---
title: Configuring Now Assist for Financial Services Operations \(FSO\)
description: Plan and configure your implementation of Now Assist for FSO. Follow the tasks listed in the configuration topics for the capabilities that you want to activate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-now-assist-skills-for-fso.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [configure now assist for fso, now assist for fso skills, activate fso now assist skills, configure case summarization, configure customer profile summarization, disputes intake virtual agent, configure fso agentic workflows]
breadcrumb: [Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configuring Now Assist for Financial Services Operations \(FSO\)

Plan and configure your implementation of Now Assist for FSO. Follow the tasks listed in the configuration topics for the capabilities that you want to activate.

-   [Configure Financial Services Operations Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-now-assist-skills.md)

    Configure Now Assist skills for Financial Services Operations to enable AI-powered capabilities such as case summarization, disputes intake, and customer profile summarization.

-   [Configure agentic workflows in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-agentic-workflows-in-fso.md)

    Activate and modify agentic workflows to enhance financial services process, such as resolving friendly fraud.

-   [Configure Financial Services Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-ai-agents.md)

    Configure Financial Services Operations AI agents for assistance with tasks such as resolving ACH disputes, and requesting support for customer research and interactions.


## Choosing a language model service provider

Different models can provide different performance and responses. You can choose which service provider to use for your Now Assist for FSO skills and agentic AI.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

**Note:** See [Federal exclusion notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md) for more information.

## Configuring ACLs

You can enable security implementation on Now Assist for FSO skills, AI agents, and agentic workflows through access control lists \(ACLs\) and user identities. These ACLs determine which users have permissions to discover and invoke these features.

Configure and manage ACLs for agentic workflows and AI agents in the AI Agent Studio. See [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md) for more details.

Predefined ACLs exist in Now Assist for FSO for the following:

-   Case summarization skills
-   Disputes intake via Virtual Agent
-   AI agents and agentic workflows in Help Resolve Friendly Fraud
-   Subflows used in Disputes intake via Virtual Agent
-   Subflows and subflow actions used in the Help Resolve Friendly Fraud agentic workflow

See [Configure an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/t_CreateAnACLRule.md) for more information on configuring ACLs.

## Role masking

Required roles: sn\_bom\_credit\_card.dispute\_agent, sn\_bom\_credit\_card.dispute\_agent\_connector.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to Resolve friendly fraud using Agentic AI.

-   **[Configure Financial Services Operations Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-now-assist-skills.md)**  
Configure Now Assist skills for Financial Services Operations to enable AI-powered capabilities such as case summarization, disputes intake, and customer profile summarization. Use this overview to identify and complete the configuration tasks for your deployment.
-   **[Configure agentic workflows in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-agentic-workflows-in-fso.md)**  
Activate and modify agentic workflows for Now Assist for FSO in AI Agent Studio.
-   **[Configure Financial Services Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-ai-agents.md)**  
Configure Financial Services Operations AI agents to define their tools, access controls, triggers, and active status. You can also review Knowledge Graph tag records that supply structured and unstructured data to improve AI agent performance.
-   **[Skill inputs for Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/skill-inputs-and-triggers-for-now-assist-for-financial-services-operations-fso.md)**  
Review the inputs for each skill to see how a skill is used.

**Parent Topic:**[Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md)

**Related topics**  


[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md)

[Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md)

[Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md)

