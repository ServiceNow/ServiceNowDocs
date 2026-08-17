---
title: Order exception AI voice agent
description: This AI voice agent helps customers request faster delivery of an order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-ord-order-exception-voice-ai-voice-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Order Management AI agents, Order Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Order exception AI voice agent

This AI voice agent helps customers request faster delivery of an order.

## Workflow

The agent validates order numbers, checks if expedited options exist, and either processes the expedite request with updated delivery details or creates an order case.

1.  Retrieve and confirm the order number.
2.  Validate the order and confirm the details.
3.  Check if expedited shipping is available for the selected order and retrieve the earliest possible delivery date. If it can be expedited, request approval or date selection from the user.
4.  If the order cannot be expedited, summarize the details and create an order case.
5.  Share the case details with the user.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Check availability and earliest delivery

Create order case

Get Customer Orders Tool

Validate and get order details


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_customerservice.customer

</td></tr><tr><td>

Data access roles

</td><td>

sn\_customerservice.customer

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Order Management at [Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md).

**Parent Topic:**[Order Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/om-ai-agents-overview.md)

