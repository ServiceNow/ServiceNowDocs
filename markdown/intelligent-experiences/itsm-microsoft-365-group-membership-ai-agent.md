---
title: Microsoft 365 group membership AI agent
description: The agent helps users add or remove members of Microsoft 365 distribution list groups. It finds the group, validates the people to add or remove, confirms the action with the user, and records the request in an incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-microsoft-365-group-membership-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Microsoft 365 group membership AI agent

The agent helps users add or remove members of Microsoft 365 distribution list groups. It finds the group, validates the people to add or remove, confirms the action with the user, and records the request in an incident.

## Workflow

The agent helps the user add or remove members of a Microsoft 365 distribution list group.

1.  Enter a query in natural language such as "Add Abel to ITSM group" to retrieve the details and understand the request.
2.  Ask the user for the group name or group email, if it was not already provided.
3.  Look up the group, and if it isn't found, tell the user and offer to try another group name.
4.  Confirm whether the user wants to add or remove members, and collect the names or email addresses.
5.  Validate the names and email addresses, asking the user to correct any errors or choose between ambiguous matches.
6.  Ask the user to explicitly confirm the add or remove action.
7.  Create an incident if the user didn't provide one, and then start the process to add or remove the members.
8.  Display a confirmation message with the results.

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

Create incident

Get details of incident

Look Up Group

Start The Process

Validate Names and Email Addresses


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Not defined.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

[IT Service Management AI agent collection Manage Microsoft 365 group members agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/now-assist-itsm-aiagents-O365-groupmembers-workflow.md)

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

