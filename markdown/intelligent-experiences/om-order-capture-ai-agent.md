---
title: Order capture AI agent
description: This AI agent helps order-management agents investigate, understand, and update customer orders in any form, whether direct \(“apply 10% discount to all lines”\), corrective \(“this address is wrong, fix it”\), bulk \(“set quantity to 50 for every item”\), diagnostic \(“why is this order delayed?”\), or follow-up \(“undo the last change”\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-order-capture-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Order Management AI agents, Order Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Order capture AI agent

This AI agent helps order-management agents investigate, understand, and update customer orders in any form, whether direct \(“apply 10% discount to all lines”\), corrective \(“this address is wrong, fix it”\), bulk \(“set quantity to 50 for every item”\), diagnostic \(“why is this order delayed?”\), or follow-up \(“undo the last change”\).

## Workflow

The agent automatically uses the currently opened order as context, validates line-item data, recognizes product and variant references, and interprets both simple and complex change requests. It then determines the safest corrective action—such as updating fields in bulk, modifying specific line items, swapping products, adding new items, removing incorrect ones, or fixing fulfillment or shipping details.

1.  Retrieve and confirm the order number.
2.  AGENT IDENTITY AND RESPONSIBILITIES.
3.  GLOBAL VARIABLES \(AGENT VARIABLE STORE\).

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

-   **Script**

bulk\_apply\_discount

create\_order\_case

create\_order\_line\_case

undo\_last\_action

Update quantity for all lines

update\_shipping\_address

-   **Unknown**

Fetch actions available for the user from Order Assist- Action Selector

find\_similar\_location

Offer to undo previous order action

-   **Record Operation**

order\_number\_from\_order\_sys\_id

order\_sys\_id\_from\_order\_number

remove\_top\_order\_line\_item

verify\_order\_line\_item


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ind\_tmt\_orm.order\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ind\_tmt\_orm.order\_agent

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Assistance for orders

</td></tr></tbody>
</table>Learn more about Order Management at [Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md).

**Parent Topic:**[Order Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/om-ai-agents-overview.md)

