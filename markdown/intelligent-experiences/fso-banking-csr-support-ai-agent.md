---
title: Banking CSR support AI agent
description: The AI agent acts as a copilot for a customer service representative on a live banking call or chat, retrieving account, transaction, balance, credit, loan, and policy information in real time and presenting it in a clear, conversational format so the representative can respond quickly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fso-banking-csr-support-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Banking CSR support AI agent

The AI agent acts as a copilot for a customer service representative on a live banking call or chat, retrieving account, transaction, balance, credit, loan, and policy information in real time and presenting it in a clear, conversational format so the representative can respond quickly.

## Workflow

The agent helps the CSR retrieve banking customer information during a live interaction and keeps the conversation moving.

1.  When the CSR opens a new customer interaction, load that interaction's context and reset any prior conversation state.
2.  Take the CSR's question — a typed banking query or a request to check for a new customer interaction — and send it, with the current customer context, to the query analysis tool.
3.  Update the tracked customer context \(name, type, and topic\) with what the tool returns.
4.  Present the results found, showing the most relevant account, transaction, case, or interaction fields, and note plainly when a value wasn't available.
5.  Add related knowledge-base information after the account results whenever the tool returns any.
6.  If nothing was found for the request, let the CSR know and offer to try again or check for a new customer interaction.
7.  End every response with a quick-action button so the CSR can continue the conversation without typing.

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

-   **Subflows**

CSR Query Analyser


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_fso\_csr.business\_agent
-   sn\_fso\_csr.personal\_agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_fso\_csr.business\_agent
-   sn\_fso\_csr.personal\_agent

</td></tr><tr><td>

Triggers

</td><td>

CSR Interaction

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/fso-ai-agents-overview.md)

