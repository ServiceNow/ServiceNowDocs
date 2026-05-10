---
title: Configuring Now Assist for Financial Services Operations \(FSO\)
description: Plan and configure your implementation of skills in Now Assist for FSO. Follow the tasks listed in the configuration overview for the skills that you want to activate.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configuring Now Assist for Financial Services Operations \(FSO\)

Plan and configure your implementation of skills in Now Assist for FSO. Follow the tasks listed in the configuration overview for the skills that you want to activate.

## Configuration overview

-   [Configure case summarization in Now Assist for Financial Services Operations \(FSO\)](../../fso-common/task/configure-now-assist-for-fso.md)

    Follow these steps to configure case summarization skills for your agents in Financial Services Workspace and Core UI.

-   [Configure customer profile summarization in Now Assist for FSO](../task/configure-customer-profile-summarization-fso.md)

    Follow these steps to configure and activate the customer profile summarization skill for the Customer 360 page in Agentic Contact Center for Banking.

-   [Configure customer interaction context summary skill in Now Assist for FSO](../task/configure-customer-contextual-summarization-fso.md)

    Follow these steps to configure and activate the customer interaction context summary skill for the Interaction page in Agentic Contact Center for Banking.

-   [Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)](../task/configuring-disputes-intake-via-virtual-agent.md)

    Follow these steps to set up Disputes intake via Virtual Agent to provide a conversational chatbot experience for your customers to submit card disputes.

-   [Configuring agentic workflows in Financial Services Operations](configuring-agentic-workflows-in-fso.md)

    Agentic workflows in FSO are inactive by default. Use AI Agent Studio to enable agentic workflows and AI agents in FSO and enhance your financial services processes.


## Choosing a language model service provider

Different models can provide different performance and responses. You can choose which service provider to use for your Now Assist for FSO skills and agentic AI.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

**Note:** See [Federal exclusion notice](../../fso-common/concept/now-assist-for-financial-services-operations.md#section_yvd_n43_qbc) for more information.

## Configuring ACLs

You can enable security implementation on Now Assist for FSO skills, AI agents, and agentic workflows through access control lists \(ACLs\) and user identities. These ACLs determine which users have permissions to discover and invoke these features.

Configure and manage ACLs for agentic workflows and AI agents in the AI Agent Studio. See [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md) for more details.

See [Configure an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/t_CreateAnACLRule.md) for more information on configuring ACLs.

**Related topics**  


[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md)

[Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md)

[Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md)

