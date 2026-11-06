---
title: Telecom Smart Actions Agent AI agent
description: The agent gathers telecom customer context from an account or consumer record and runs a pre-diagnostic sweep across product inventory and five service health checks: duplicate cases, open incidents, work orders, alerts, and outstanding billing. It then produces a support summary and answers follow-up questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-telecom-smart-actions-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Telecommunications Customer 360 AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Telecom Smart Actions Agent AI agent

The agent gathers telecom customer context from an account or consumer record and runs a pre-diagnostic sweep across product inventory and five service health checks: duplicate cases, open incidents, work orders, alerts, and outstanding billing. It then produces a support summary and answers follow-up questions.

## Workflow

The agent assembles the customer context and service health picture that a human agent needs before diagnosing a telecom issue.

1.  Resolve the account or the consumer from the record that triggered the agent and display the customer context.
2.  Retrieve the product inventory for the account or the consumer.
3.  Enrich the customer context from the knowledge graph.
4.  Check for duplicate cases.
5.  Check for open incidents, open work orders, and open alerts.
6.  Check for outstanding billing.
7.  Display a customer 360 summary with the risk level, any correlation between the findings, and a recommended next action.
8.  Answer the human agent's follow-up questions from the context already gathered, and close the conversation when the agent indicates that they are done.

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

-   **Script**

CheckDuplicateCases

CheckOpenAlerts

CheckOpenIncidents

CheckOpenWorkOrders

CheckOutstandingBilling

CheckProductInventory

GetRecordContext

-   **Tool**

Gather information from knowledge graph


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_tmt\_agentic\_ai.smart\_actions\_agent
-   snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Smart Actions for Telecom

</td></tr></tbody>
</table>Learn more about Telecommunications Customer 360 at [Telecommunications Customer 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-land-page.md).

**Parent Topic:**[Telecommunications Customer 360 AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/c360-ai-agents-overview.md)

