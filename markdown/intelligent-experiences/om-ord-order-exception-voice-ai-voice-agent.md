---
title: Order exception AI voice agent
description: This AI voice agent helps customers change an order after they place it. Customers can request faster delivery, a higher quantity, or a different shipping location, in any combination, for one order line. The agent creates one case for the requested changes and can connect the customer to a live agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-ord-order-exception-voice-ai-voice-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Order Management AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Order exception AI voice agent

This AI voice agent helps customers change an order after they place it. Customers can request faster delivery, a higher quantity, or a different shipping location, in any combination, for one order line. The agent creates one case for the requested changes and can connect the customer to a live agent.

## Workflow

The agent captures every change the customer asks for on one order line, validates new shipping locations, creates one case, and hands off to a live agent when it can't complete the request.

1.  Listen to the customer's request and identify each change they want: faster delivery, a higher quantity, a different shipping location, or any combination of these.
2.  Retrieve the order by product name, order number, or a list of the customer's recent orders, and confirm the order with the customer.
3.  Retrieve the order line items and confirm the line to change. The agent handles one line per case.
4.  Ask only for missing values, such as the new quantity, the required delivery date, or the new shipping location.
5.  Validate a new shipping location and confirm the matching address with the customer.
6.  Ask whether the customer wants to change anything else on the same line before submitting.
7.  Read back all requested changes for a final confirmation, and create one order case for them.
8.  Share the case number and a summary of the original and requested values.
9.  End the conversation. If the customer asks for more changes after the case is created, or the agent can't complete the request after three attempts or a tool failure, transfer the customer to a live agent with the case and conversation summary.

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

Check availability and earliest delivery

Create order case

Get Customer Orders Tool

Get Order Line Items

Validate Address

Validate and get order details


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_customerservice.customer

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_customerservice.customer

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about customer self-service via Business Portal at [Customer self-service for Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-self-service-business-portal.md).

**Parent Topic:**[Order Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/om-ai-agents-overview.md)

