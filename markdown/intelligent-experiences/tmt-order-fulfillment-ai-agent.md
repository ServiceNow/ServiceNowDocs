---
title: Order fulfillment AI agent
description: The AI agent finds the tasks needed to fulfill a domain order. It uses historical data from similar domain orders to suggest tasks, and it creates the tasks after the user confirms them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/tmt-order-fulfillment-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-11-04"
reading_time_minutes: 2
breadcrumb: [Sales CRM for Telecommunications AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Order fulfillment AI agent

The AI agent finds the tasks needed to fulfill a domain order. It uses historical data from similar domain orders to suggest tasks, and it creates the tasks after the user confirms them.

## Workflow

The agent helps the user identify and create the fulfillment tasks for a domain order.

1.  Retrieve the domain order details.
2.  Look for historical fulfillment tasks for the domain order, or identify the available fulfillment tasks when no history exists.
3.  Present the suggested tasks to the user.
4.  Ask the user to confirm the task list, or let them enter their own tasks, which the agent validates and shows back for confirmation.
5.  Create the confirmed fulfillment tasks.
6.  Update the trigger task to completed.
7.  Show the user a summary of the steps taken and the tasks that were created.

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

-   **Script**

Create Fulfillment Tasks

Fetch Domain Order record details.

Find available Fulfillment tasks for given specification

Find historic fulfillment tasks

Update Trigger task state.

Validate task names


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_gaf.data\_writer
-   sn\_ind\_tmt\_orm.order\_fulfilment\_agent

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

Not applicable.

</td></tr></tbody>
</table>Learn more about Sales CRM for Telecommunications at [Sales Customer Relationship Management for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/sales-crm.md).

**Parent Topic:**[Sales CRM for Telecommunications AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/somt-ai-agents-overview.md)

