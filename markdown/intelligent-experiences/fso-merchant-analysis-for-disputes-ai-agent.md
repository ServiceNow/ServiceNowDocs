---
title: Merchant analysis for disputes AI agent
description: The agent evaluates the merchant behind a disputed transaction for credibility. It researches the merchant's reputation and regulatory history, weighs the evidence against a set of rules, and recommends whether the merchant is credible, with a rationale the human agent can accept or override.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fso-merchant-analysis-for-disputes-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Merchant analysis for disputes AI agent

The agent evaluates the merchant behind a disputed transaction for credibility. It researches the merchant's reputation and regulatory history, weighs the evidence against a set of rules, and recommends whether the merchant is credible, with a rationale the human agent can accept or override.

## Workflow

The agent helps the human agent assess whether a disputed transaction's merchant is credible.

1.  Look up the merchant details for the disputed transaction and confirm the required task data is present.
2.  Display the task's case, transaction, customer, dispute amount, and reason code.
3.  Search the web for information about the merchant's reputation, complaints, and regulatory history, prioritizing government and regulatory sources — or fall back to analyzing the case details alone if search is unavailable.
4.  Weigh the findings against a set of credibility rules to determine whether the merchant is credible or not.
5.  Present the credibility assessment and its rationale, then ask the agent to agree or disagree.
6.  If the agent disagrees, ask for their reasoning and record the opposite assessment instead.
7.  Record the final credibility outcome and reasoning on the task, and close the conversation.

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

-   **Flow Actions**

Get Merchant Details From Task

-   **Record Operations**

Set AI recommendation

-   **Scripts**

AI Credibility Determination Logic

Fetch Task Details

Update Merchant Analysis Final Outcome And Close The Task

-   **Web searches**

Web search


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_bom\_credit\_card.dispute\_agent
-   sn\_bom\_credit\_card.dispute\_agent\_connector

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_bom\_credit\_card.dispute\_agent
-   sn\_bom\_credit\_card.dispute\_agent\_connector

</td></tr><tr><td>

Triggers

</td><td>

Merchant analysis task

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

