---
title: Using agentic AI in Now Assist for Customer Service Management \(CSM\)
description: The Customer Service Management \(CSM\) AI Agent Collection provides a set of prebuilt, fully configured AI agents and agentic workflows designed to address common Customer Service Management scenarios.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Now Assist for CSM, Customer Service Management]
---

# Using agentic AI in Now Assist for Customer Service Management \(CSM\)

The Customer Service Management \(CSM\) AI Agent Collection provides a set of prebuilt, fully configured AI agents and agentic workflows designed to address common Customer Service Management scenarios.

These model examples combine autonomous and supervised flows to perform multi-step actions using advanced reasoning, triggered by customer cases, conversations, or detected intents. Built on the ServiceNow AI Platform, the agents leverage capabilities such as Knowledge Graph, Flow Designer, scripting, Topics, Catalog Items, Retrieval-Augmented Generation \(RAG\), record operations, web search, and generative inputs. Powered by AI Agent Fabric and Workflow Data Fabric, the collection operates seamlessly across systems without dependency on data location, while Guardian enforces guardrails for security and compliance. By offering ready-to-use building blocks, it helps guide and automate complex processes, reduce agent friction, and free human agents to focus on higher-value work—ultimately accelerating resolution times and enhancing customer experience.

<table id="table_xt1_lth_l2c"><thead><tr><th>

Agentic workflow

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

</td></tr><tr><td>

[Complaint Case AI Agent collection](csm-ai-agents-use-cases.md)

</td><td>

Automate and enhance the complaint resolution process by gathering missing information, detecting customer sentiment, categorizing complaints, and proposing resolutions. It supports human agents by managing complaint intake, triage, research, resolution, and ongoing communication, reducing manual effort and case closure time. 

</td><td>

-   Complaint case intake agent
-   Complaint case triage agent
-   Complaint case research agent
-   Complaint case summarization skill

</td></tr></tbody>
</table>## Supported Large Language Models

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see Implement access control in Now Assist AI agents

## Considerations for running the autonomous AI Agents

**Important:** By default, all agentic workflows and AI agent records are read only.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

## Standalone AI agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

