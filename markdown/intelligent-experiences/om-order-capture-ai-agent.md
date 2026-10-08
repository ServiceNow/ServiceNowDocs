---
title: Order capture AI agent
description: The Order capture AI agent helps you create orders from quote lines or uploaded files, and manage, investigate, and update existing orders. For example, you can apply discounts, change quantities, fix shipping addresses, remove lines, create cases, and undo changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/om-order-capture-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Order Management AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Order capture AI agent

The Order capture AI agent helps you create orders from quote lines or uploaded files, and manage, investigate, and update existing orders. For example, you can apply discounts, change quantities, fix shipping addresses, remove lines, create cases, and undo changes.

## Workflow

The agent runs in three modes: Quote Ingest, File Upload Ingest, and Manage Order. It creates orders from quote lines or uploaded files, and it helps you investigate and update existing orders.

1.  The agent detects the mode from your input: a quote starts Quote Ingest mode, an uploaded file starts File Upload Ingest mode, and an order number or open order starts Manage Order mode.
2.  In Quote Ingest mode, the agent reads the quote lines, groups them into orders by account and any configured order-splitting rules, and creates the orders.
3.  In File Upload Ingest mode, the agent extracts order data from the uploaded file, maps the file columns to order fields, and creates the orders in bulk.
4.  During ingest, the agent records any line it can't resolve, such as an unknown product or account, as an item for you to resolve in Action Center.
5.  After ingest, the agent gives you a summary of the created orders with a link to each order.
6.  In Manage Order mode, the agent uses the currently opened order as context and shows you the actions available for the order's current state.
7.  After you select an action, the agent validates the order and line-item data and applies the change, such as a bulk discount, a quantity update, a shipping address fix, a line removal, or a new case.
8.  When an action is reversible, the agent offers to undo it.

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

Attach Order To Group

bulk\_apply\_discount

check\_product\_offering

Compute Group Key

Create All Orders From Run

Create Header Followup

Create Line Followup

Create Order Header

Create Order Line

Create Orders From Run

Create Single Order

create\_order\_case

create\_order\_line\_case

Extract Splitting Fields

Fail Ingest Run

Fetch actions available for the user from Order Assist- Action Selector

Finalize Ingest Run

find\_account\_by\_name

find\_consumer\_by\_name

find\_quote\_by\_number

find\_similar\_location

Get agent settings

Get Followup Issues

Get Open Action Items

Get Order Schema Fields

Get Quote Lines

Get Unresolved Issues

get\_order\_followups

Group line data

Initialize Run Followups

Mark Header Successful

Mark Line Successful

Offer to undo previous order action

Parse Attachment Headers

Prepare Reprocess

Read Attachment Content

Read Ingest Run Lines

Record Correction

Record Followup Correction

Record Line Failure

Reprocess Followup

resolve\_reference

Save Column Mapping

Start Ingest Run

Suppress Followup

undo\_last\_action

Unsuppress Followup

Update Action Item Error

Update agent config

Update Ingest Run

Update Order Followup

Update quantity for all lines

Update Quote Work Note

update\_shipping\_address

Upload order splitting rules

validate\_account\_sys\_id

-   **Subflows**

Order Assist DocIntel

-   **Record operations**

order\_number\_from\_order\_sys\_id

order\_sys\_id\_from\_order\_number

remove\_top\_order\_line\_item

verify\_order\_line\_item

-   **Capabilities**

Extract information from documents


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   admin
-   sn\_ind\_tmt\_orm.order\_admin
-   sn\_ind\_tmt\_orm.order\_agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   admin
-   platform\_ml\_di.extraction\_agent
-   sn\_ind\_tmt\_orm.order\_admin
-   sn\_ind\_tmt\_orm.order\_agent
-   sn\_order\_case.agent
-   sn\_quote\_mgmt\_core.quote\_writer
-   snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Assistance for orders

</td></tr></tbody>
</table>Learn more about Order Management at [Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/explore-order-management.md).

**Parent Topic:**[Order Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/om-ai-agents-overview.md)

