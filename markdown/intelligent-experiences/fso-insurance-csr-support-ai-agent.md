---
title: Insurance CSR support AI agent
description: The agent gives a customer service representative \(CSR\) real-time answers during a live insurance call, either from a typed question or from the latest call transcript, retrieving the customer's policy, coverage, claim, and billing data or knowledge-base guidance so the CSR can respond quickly without switching screens.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fso-insurance-csr-support-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Insurance CSR support AI agent

The agent gives a customer service representative \(CSR\) real-time answers during a live insurance call, either from a typed question or from the latest call transcript, retrieving the customer's policy, coverage, claim, and billing data or knowledge-base guidance so the CSR can respond quickly without switching screens.

## Workflow

The agent helps the CSR answer a customer's insurance question during a live call, whether typed directly or picked up from the call transcript.

1.  When the CSR selects **Get customer request**, read the latest call transcript to pick up the customer's most recent question; otherwise take the CSR's typed question directly.
2.  Classify the question as a general knowledge question, a product-catalog question, or a question about the customer's own records, and confirm it's within scope — insurance policies, coverages, claims, servicing cases, or procedures.
3.  If the question refers to a record picked from an earlier list, resolve which record it means, asking the CSR to confirm when it's ambiguous.
4.  If the question asks about a sub-record like coverages or beneficiaries without naming the parent policy or claim, first look up the matching parent records and ask the CSR which one to use.
5.  Look up the customer's data, relevant product information, and knowledge-base guidance as needed to answer the question.
6.  Present the results — as a list, a single record's details, a sub-record breakdown, or a short summary, depending on what was asked — citing the knowledge-base source when guidance is included.
7.  Let the CSR know when nothing was found, then offer to pull the next customer request and wait for the next question.

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

-   **Scripts**

Conversation Transcript Reader

-   **Subflows**

Insurance Data Lookup


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_ins\_csr.claims\_agent
-   sn\_ins\_csr.servicing\_agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_ins\_csr.claims\_agent
-   sn\_ins\_csr.servicing\_agent

</td></tr><tr><td>

Triggers

</td><td>

CSR Interaction for Insurance

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

