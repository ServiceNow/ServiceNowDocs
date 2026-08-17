---
title: Create work order AI agent
description: This AI agent creates work orders using text descriptions and image.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fsm-create-work-order-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Field Service Management AI agents, Field Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Create work order AI agent

This AI agent creates work orders using text descriptions and image.

## Workflow

The agent helps users complete tasks related to create work order.

1.  Receive the user's request and validate required inputs.
2.  Execute the appropriate tools to perform the requested action.
3.  Return the results or update the relevant record.

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

-   **Subflow**

Submit and Fetch Results

-   **Conversational topic**

upload image

-   **Scripts**

Attach the image to the work order

Get attachment sys id from media link

Create and update work order for image


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

wm\_agent

</td></tr><tr><td>

Data access roles

</td><td>

wm\_agent

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

Create a work order

</td></tr></tbody>
</table>Learn more about  at [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ext-cont-connectors-landing-page.md).

**Parent Topic:**[Field Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/fsm-ai-agents-overview.md)

