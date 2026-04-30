---
title: Use agentic AI in Now Assist for Integrated Risk Management \(IRM\)
description: Use agents within an agentic workflow or as standalone agents to achieve specific automated outcomes.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-11-10"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Use agentic AI in Now Assist for Integrated Risk Management \(IRM\)

Use agents within an agentic workflow or as standalone agents to achieve specific automated outcomes.

Find information such as the large language models \(LLM\) supported in Now Assist and security controls that are important considerations for using agentic AI.

For more information on language support, see [Multilingual service for Now Assist](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and [Multilingual support for ServiceNow generative AI products](https://www.servicenow.com/community/now-assist-articles/multilingual-support-for-servicenow-generative-ai-products/ta-p/3099258).

## Supported large language models \(LLM\)

**Note:**

-   You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   For the Now LLM Service updates, see [Now LLM Service updates](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user.For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Considerations for running the autonomous AI Agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.
-   Azure OpenAI is recommended for Now Assist for IRM agentic workflows.

## Standalone AI agents

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

For information on the standalone Now Assist for IRM AI agents, see [Standalone AI Agents in Now Assist for Integrated Risk Management \(IRM\) skills](standalone-ai-agents-in-risk-sustainability.md).

