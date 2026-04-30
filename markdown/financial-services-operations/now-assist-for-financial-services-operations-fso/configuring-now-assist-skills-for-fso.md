---
title: Configuring Now Assist for Financial Services Operations \(FSO\)
description: Plan and configure your implementation of skills in Now Assist for FSO. Follow the tasks listed in the configuration overview for the skills that you want to activate.
locale: en-US
release: yokohama
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Now Assist for Financial Services Operations \(FSO\)]
---

# Configuring Now Assist for Financial Services Operations \(FSO\)

Plan and configure your implementation of skills in Now Assist for FSO. Follow the tasks listed in the configuration overview for the skills that you want to activate.

## Configuration overview

-   [Configure case summarization in Now Assist for Financial Services Operations \(FSO\)](../../fso-common/task/configure-now-assist-for-fso.md)

    Configure the application so that your agents can use case summarization skills in Financial Services Workspace and Core UI.

-   [Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)](../task/configuring-disputes-intake-via-virtual-agent.md)

    Set up Disputes intake via Virtual Agent to provide a conversational chatbot experience for your customers to submit card disputes.

-   [Configuring agentic workflows in Financial Services Operations](configuring-agentic-workflows-in-fso.md)

    Use AI Agent Studio to enable agentic workflows in FSO and enhance your financial services processes with the help of AI agents.


## Choosing a language model service provider

Different models can provide different performance and responses. You can choose which service provider to use for your Now Assist for FSO skills and agentic AI.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Configuring security

You can enable security implementation on Now Assist for FSO skills, AI agents, and agentic workflows through access control lists \(ACLs\) and user identities. These ACLs determine which users have permissions to discover and invoke these features. See [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information on configuring ACLs.

Configure and manage ACLs for agentic workflows and AI agents in the AI Agent Studio. See [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more details.

Predefined ACLs exist in Now Assist for FSO for the following:

-   Case summarization skills
-   Disputes intake via Virtual Agent
-   AI agents and agentic workflows in Help Resolve Friendly Fraud
-   Subflows used in Disputes intake via Virtual Agent
-   Subflows and subflow actions used in the Help Resolve Friendly Fraud agentic workflow

**Related topics**  


[Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

[Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

