---
title: Order fulfillment AI agent
description: This Sales Customer Relationship Management agent identifies fulfillment tasks for a domain order by checking historic tasks from similar orders, confirms the task list with the user, and creates them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/som-order-fulfillment-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales Automation, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Order fulfillment AI agent

This Sales Customer Relationship Management agent identifies fulfillment tasks for a domain order by checking historic tasks from similar orders, confirms the task list with the user, and creates them.

## Workflow

1.  Fetch the details for the given domain order number.
2.  Check for existing historic fulfillment tasks for the order and display any that are found.
3.  Present the task list and ask the user to confirm. If rejected, let the user provide their own task list, validate it, and confirm again.
4.  Create the fulfillment tasks in the system.
5.  Update the trigger task status to completed.
6.  Display a mandatory summary of all steps taken, including each created task's name and sys\_id.

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

Create fulfillment tasks

Fetch domain order record details.

Find available fulfillment tasks for given specification

Find historic fulfillment tasks

Update trigger task state.

Validate task names


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_somt\_gen\_ai.sales\_and\_order\_fulfillment\_ai\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ind\_tmt\_orm.order\_fulfilment\_agent, sn\_gaf.data\_writer

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

Not applicable.

</td></tr></tbody>
</table>Learn more about Sales Customer Relationship Management at [Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-overview.md).

**Parent Topic:**[Sales Automation AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sales-automation-ai-agents-overview.md)

