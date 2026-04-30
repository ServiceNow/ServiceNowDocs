---
title: Using Troubleshooting steps identification AI agent
description: The Troubleshooting steps identification AI agent fetches the context from a case, identifies the missing context by comparing it with knowledge articles, similar cases, and standard operating documents, and then proposes additional troubleshooting steps.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [AI Agents, Agentic AI]
breadcrumb: [Use generative AI skills, Now Assist for CSM, Customer Service Management]
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

## Access control lists \(ACLs\)

Access Control Lists \(ACLs\) are preconfigured for the troubleshooting steps identification AI Agent, including their associated flows and actions. By default, ACLs are configured for the sn\_esm\_agent role. Customers can modify these ACLs to align with their specific business requirements and security policies.

To manually update ACLs for custom roles:

1.  Go to the **sys\_security\_acl** table.
2.  Use filters to locate ACLs related to your use case, AI agent, and internal flows or actions.
3.  Add your custom role to each relevant ACL record.

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](now-assist-csm-using.md)

**Related topics**  


[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

[Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

