---
title: Standard change template proposal AI agent
description: Provided with a change request, this AI agent searches for similar changes and returns a list of similar changes to use for a proposal record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-standard-change-template-proposal-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Standard change template proposal AI agent

Provided with a change request, this AI agent searches for similar changes and returns a list of similar changes to use for a proposal record.

## Workflow

When the user chooses the changes that are appropriate for the template, this agent generates the content for multiple fields and creates a proposal template record.

1.  Ask for the change request number.
2.  Fetch similar change requests.
3.  Use the Fetch standard change mandatory fields tool to return the fields and value list of the selected changes.
4.  Analyze the field values to create template values.
5.  If the user approves, generate the template.
6.  Use the template to create a change template proposal record.

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

Fetch similar changes

Fetch standard change mandatory fields

Standard change proposal record creator


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

change\_manager, itil

</td></tr><tr><td>

Data access roles

</td><td>

change\_manager, itil

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Generate change template proposal record

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

