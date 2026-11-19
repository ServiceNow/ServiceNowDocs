---
title: Telco order fulfilment template creation AI agent
description: The AI agent generates a task plan template from the specification and dependency JSON provided to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-telco-order-fulfilment-template-creation-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-11-04"
reading_time_minutes: 2
breadcrumb: [Sales CRM for Telecommunications AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI assets, Enable AI experiences]
---

# Telco order fulfilment template creation AI agent

The AI agent generates a task plan template from the specification and dependency JSON provided to it.

## Workflow

The agent helps the user create a task plan template for a specification, using task and dependency data passed to it by the workflow.

1.  Retrieve the available order intent types and ask the user to select one or more actions for the template.
2.  Create the task plan template record for the specification, using the selected actions and the dependency data.
3.  Show a summary of the template, including its number, the number of tasks and task dependencies, and a link to the template.
4.  Tell the user that the template must be confirmed and published from the link.

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

Create Task Plan Record

Fetch Order Intent Type


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_prd\_pm.product\_catalog\_admin
-   sn\_task\_plan.creator

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

Design Telecom Order Fulfilment Template

</td></tr></tbody>
</table>Learn more about Sales CRM for Telecommunications at [Sales Customer Relationship Management for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/sales-crm.md).

**Parent Topic:**[Sales CRM for Telecommunications AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/somt-ai-agents-overview.md)

