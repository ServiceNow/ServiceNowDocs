---
title: ACH dispute return recommendation AI agent
description: The AI agent guides the human agent through a structured decision-making process to determine the best action for an ACH dispute return task. The ACH dispute return recommendation AI agent analyzes disputed transactions based on merchant analysis and Nacha eligibility. The agent recommends actions based on historical data, and applies predefined rules when data is limited.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/fso-ach-dispute-return-recommendation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI assets, Enable AI experiences]
---

# ACH dispute return recommendation AI agent

The AI agent guides the human agent through a structured decision-making process to determine the best action for an ACH dispute return task. The ACH dispute return recommendation AI agent analyzes disputed transactions based on merchant analysis and Nacha eligibility. The agent recommends actions based on historical data, and applies predefined rules when data is limited.

## Workflow

The AI agent helps the human agent decide how to resolve an ACH dispute return task.

1.  Look up the ACH dispute task and display the case, transaction, customer, dispute amount, and reason code.
2.  Check historical records for similar disputes with the same reason code and outcome.
3.  Determine a recommended action — deny, file a return, or follow up with the ODFI — based on the merchant analysis and NACHA operating guidelines findings, using historical patterns when enough exist.
4.  Present the recommendation and its supporting rationale, then ask the human agent to confirm or disagree.
5.  If the human agent disagrees, let them choose an alternative action and provide a reason for the change.
6.  Record the final action and reasoning on the dispute task.
7.  Close the conversation once the task is updated.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Record Operations**

Set AI recommendation

-   **Scripts**

Fetch historical data count

Fetch most recommended frequent record

Get recommendation for non historical data

Retrieve record data

Search retrieval script

Updating the record


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

Recommendation Analysis Trigger

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/fso-ai-agents-overview.md)

