---
title: Case action AI agent
description: This agent can preform actions for the customer, including case actions \(Create a case task, Update work notes, etc.\) and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-case-action-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Case action AI agent

This agent can preform actions for the customer, including case actions \(Create a case task, Update work notes, etc.\) and more.

## Workflow

The agent helps users complete tasks related to case action.

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

-   **Subflows**

Create case task

-   **Flow Action**

Update source record worknotes


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_esm\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

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

Provide customer 360 insights

</td></tr></tbody>
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md).

**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/csm-ai-agents-overview.md)

