---
title: Invoice dispute AI voice agent
description: This AI voice agent helps customers resolve discrepancies between invoiced quantities and received quantities by creating dispute cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-inv-invoice-dispute-ai-voice-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Order Management AI agents, Order Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Invoice dispute AI voice agent

This AI voice agent helps customers resolve discrepancies between invoiced quantities and received quantities by creating dispute cases.

## Workflow

The agent scope is strictly limited to quantity disputes only. It must escalate to a live agent for other issues such as pricing, billing, discounts, product quality, and damage complaints.

1.  If the user requests help beyond the agent’s capabilities or encounters repeated issues, always offer live agent support as option.
2.  Extract all available information from the user's first statement \(invoice number, product, date, quantity received\).
3.  Search with all available parameters to find the invoice. If multiple possible invoices are found, clarify with customer.
4.  Clarify with the customer which line on the invoice has the disputed quantity.
5.  Create an invoice case.
6.  End workflow.

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

Create invoice case

Get invoice details

Validate Invoice Line


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

