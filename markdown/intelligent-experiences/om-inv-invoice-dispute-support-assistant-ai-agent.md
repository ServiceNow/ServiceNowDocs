---
title: Invoice dispute support assistant AI agent
description: This agent helps users efficiently identify, review, and answer questions related to invoice disputes. It validates information, maintains data integrity, and answers questions regarding the invoice case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-inv-invoice-dispute-support-assistant-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Order Management AI agents, Order Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Invoice dispute support assistant AI agent

This agent helps users efficiently identify, review, and answer questions related to invoice disputes. It validates information, maintains data integrity, and answers questions regarding the invoice case.

## Workflow

The agent can offer assistance to the user for resolving or closing invoice disputes and fetching similar invoice cases to help with invoice case resolution.

1.  Identify and confirm the invoice number with the customer.
2.  Use the Validate invoice case and fetch invoice tool to validate the invoice case number.
3.  Provide the user with a list of options, such as viewing invoice details, find similar invoice cases, and closing the case.

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

Close invoice dispute

Fetch similar invoice cases

Validate invoice case and fetch invoice

Validate invoice dispute

-   **Conversational topic**

Fetch invoice case number and interaction id


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_otc.account\_receivable\_agent, sn\_csm\_invoice.agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_otc.account\_receivable\_agent, sn\_csm\_invoice.agent

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Invoice Dispute Assist

</td></tr></tbody>
</table>Learn more about Order Management at [Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md).

**Parent Topic:**[Order Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/om-ai-agents-overview.md)

