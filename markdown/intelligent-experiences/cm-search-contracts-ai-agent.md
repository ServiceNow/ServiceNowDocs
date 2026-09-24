---
title: Search contracts AI agent
description: This AI agent helps legal professionals, procurement teams, sales executives, and compliance officers find and understand legal contracts through conversational search and Q&amp;A. It classifies each query, retrieves matching contract metadata or content, and links directly to results, while declining requests to draft, modify, or legally interpret contracts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cm-search-contracts-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Contract Management Pro AI agents, Contract Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Search contracts AI agent

This AI agent helps legal professionals, procurement teams, sales executives, and compliance officers find and understand legal contracts through conversational search and Q&amp;A. It classifies each query, retrieves matching contract metadata or content, and links directly to results, while declining requests to draft, modify, or legally interpret contracts.

## Workflow

The agent searches and answers questions about legal contracts on the user's behalf.

1.  Determine if the request is for retrieving an attachment from a contract, and if so, retrieve the attachment directly.
2.  Otherwise, classify the query as structured \(metadata-based\), unstructured \(content-based\), or a combination of both.
3.  Run the appropriate contract search based on that classification and check whether matching results were found.
4.  If matching results are found, let the user know they can select "Show" to view them; if not, ask the user to rephrase or broaden their search.
5.  Ask for clarification before acting on an ambiguous query instead of guessing what the user means.
6.  Politely decline any request that goes beyond factual contract search, such as drafting, modifying, or legally interpreting a contract, and offer to help with a supported request instead.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Subflow**

Contract information retrieval

-   **Generative AI Skill**

Contracts query classifier

-   **Script**

Retrieve attachments of a Record


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_cm\_gen\_ai.ai\_contract\_fulfiller

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_cm\_gen\_ai.ai\_contract\_fulfiller, sn\_lg\_ops.request\_fulfiller, sn\_cm\_core.contract\_fulfiller, contract\_manager, sn\_cm\_obligation.obligation\_fulfiller

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

[Conversational contract search and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cmpro-agentic-use-conv-search.md)

</td></tr></tbody>
</table>For more information, see [Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-cmpro-landing-page.md).

**Parent Topic:**[Contract Management Pro AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/cm-ai-agents-overview.md)

