---
title: Using agentic workflows in Now Assist for Customer Service Management \(CSM\)
description: The Customer Service Management \(CSM\) AI Agent Collection provides a set of prebuilt, fully configured AI agents and agentic workflows designed to address common Customer Service Management scenarios.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Using agentic workflows in Now Assist for Customer Service Management \(CSM\)

The Customer Service Management \(CSM\) AI Agent Collection provides a set of prebuilt, fully configured AI agents and agentic workflows designed to address common Customer Service Management scenarios.

These model examples combine autonomous and supervised flows to perform multi-step actions using advanced reasoning, triggered by customer cases, conversations, or detected intents. Built on the ServiceNow AI Platform, the agents leverage capabilities such as Knowledge Graph, Flow Designer, scripting, Topics, Catalog Items, Retrieval-Augmented Generation \(RAG\), record operations, web search, and generative inputs. Powered by AI Agent Fabric and Workflow Data Fabric, the collection operates seamlessly across systems without dependency on data location, while Guardian enforces guardrails for security and compliance. By offering ready-to-use building blocks, it helps guide and automate complex processes, reduce agent friction, and free human agents to focus on higher-value work—ultimately accelerating resolution times and enhancing customer experience.

<table id="table_xt1_lth_l2c"><thead><tr><th>

agentic workflow

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

[Triage cases](case-resolving-use-case.md)

</td><td>

Handles end-to-end case or case type validation, creation, verification, and escalation. It can also retrieve relevant context and details from the provided case or interaction to address customer inquiries directly and avoid unnecessary case creation.

</td><td>

-   Triage cases WrapUp
-   Context validator
-   Informational queries
-   Case creation
-   Entity extraction
-   Document verification
-   Email response

</td></tr><tr><td>

[Provide customer 360 insights](customer-service-management-ai-agent-collection-customer-360.md)

</td><td>

Provides agents with real-time, context aware responses to queries on customer data, case details, product information, catalog entries, and interaction history, using multi-turn Q&amp;A to maintain conversational context and accuracy.

</td><td>

-   Customer insight AI Agent
-   Case action AI Agent

</td></tr></tbody>
</table>## Supported Large Language Models

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

## Considerations for running the autonomous AI Agents

**Important:** By default, all agentic workflows and AI agent records are read only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

For information about Triage cases, see [Customer Service Management AI agent collection triage cases agentic workflow](case-resolving-use-case.md).

## Standalone AI agents

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

