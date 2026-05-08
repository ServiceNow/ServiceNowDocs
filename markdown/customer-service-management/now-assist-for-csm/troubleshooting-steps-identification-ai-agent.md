---
title: Using Troubleshooting steps identification AI agent
description: The Troubleshooting steps identification AI agent fetches the context from a case, identifies the missing context by comparing it with knowledge articles, similar cases, and standard operating documents, and then proposes additional troubleshooting steps.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [AI Agents, Agentic AI]
breadcrumb: [Use generative AI, Now Assist for CSM, Customer Service Management]
---

# Using Troubleshooting steps identification AI agent

The Troubleshooting steps identification AI agent fetches the context from a case, identifies the missing context by comparing it with knowledge articles, similar cases, and standard operating documents, and then proposes additional troubleshooting steps.

## Troubleshooting steps identification AI agent overview

![Troubleshooting steps identification AI agent providing suggested resolution steps for a case.](../image/nowassist-troubleshooting-agent.png)

This agent is typically used in standalone mode. Any agentic workflow that interacts with Customer Service Management \(CSM\) cases can use it.

This AI agent does the following actions:

-   Gathers the context from the case, including the attempted steps.
-   Identifies the missing context by analyzing the similar cases, knowledge base articles, and Standard Operating Procedure \(SOP\) documents that are attached to knowledge base articles.
-   Proposes additional troubleshooting steps.

Agentic workflows can access this AI agent in Core UI or CSM/FSM workspace.

## Configure AI Search for the Troubleshooting steps identification AI agent

You must configure AI Search so that this AI agent can fetch similar cases and relevant knowledge articles For more information, see [Configure AI Search to use with the Troubleshooting steps identification AI agent](../task/configure-ai-search-troubleshooting-ai-agent.md) and [Configure the Troubleshooting steps identification AI agent to use the Search retrieval tool](../task/enhance-search-retrieval-tool-troubleshooting-steps-ai-agent.md).

## Limitations

The document types supported for AI Search and document processing are:

-   Microsoft Word \(.docx\)

-   Plain Text \(.txt\)

-   Portable Document Format \(.pdf\)


When fetching text from knowledge articles, this AI agent can fetch only the **article\_body** field from the kb\_knowledge table.

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](now-assist-csm-using.md)

**Related topics**  


[bundle-platai.ai-agent-studio]

[bundle-platai.find-ai-agents]

[bundle-platai.na-ai-agents]

[bundle-platai.install-ai-agents-plugins]

