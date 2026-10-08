---
title: Nacha operating guidelines check AI agent
description: The agent determines whether a return code assigned to a disputed transaction is eligible for filing. It checks the case against NACHA operating guidelines' time-frame and documentation requirements and presents its eligibility decision and reasoning to the human agent for confirmation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fso-nacha-operating-guidelines-check-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Nacha operating guidelines check AI agent

The agent determines whether a return code assigned to a disputed transaction is eligible for filing. It checks the case against NACHA operating guidelines' time-frame and documentation requirements and presents its eligibility decision and reasoning to the human agent for confirmation.

## Workflow

The agent helps the human agent confirm whether a return code is eligible for filing under NACHA rules.

1.  Look up the return code eligibility task and confirm the return code is present.
2.  Display the case, transaction, customer, dispute amount, and reason code details.
3.  Fetch the NACHA return-code eligibility guidelines and the customer's intake responses for the transaction.
4.  Check the return code's eligibility against the guidelines' time-frame limit and Written Statement of Unauthorized Debit \(WSUD\) requirement.
5.  Present the eligibility decision and its rationale, then ask the agent to agree or disagree.
6.  If the agent disagrees, ask for their reasoning and reverse the eligibility decision accordingly.
7.  Record the final eligibility outcome and reasoning on the task, and confirm closure with the agent.

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

-   **Record Operations**

Set AI recommendation

-   **Scripts**

Fetch intake responses

Update eligibility final outcome and close task

-   **Search retrievals**

Get knowledge article

-   **Subflows**

Get return code eligibility task details


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

Nacha operating guidelines evaluation task

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

