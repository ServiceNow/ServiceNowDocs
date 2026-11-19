---
title: Microsoft Active Directory computer management AI agent
description: This AI agent manages Microsoft Active Directory computer accounts. It creates, updates, enables, disables, and deletes computers, looks up computers, and checks whether a computer exists or is disabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/inth-ms-ad2-microsoft-active-directory-computer-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Microsoft Active Directory v2 Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI assets, Enable AI experiences]
---

# Microsoft Active Directory computer management AI agent

This AI agent manages Microsoft Active Directory computer accounts. It creates, updates, enables, disables, and deletes computers, looks up computers, and checks whether a computer exists or is disabled.

## Workflow

The agent helps the user manage computer accounts in Microsoft Active Directory.

1.  Ask the user what they want to do and collect the details the action needs, such as the computer name.
2.  Look up a computer or check whether it exists.
3.  Check whether a computer is disabled.
4.  Create a new computer account or update an existing one.
5.  Enable or disable a computer.
6.  Delete a computer account.
7.  Report the outcome to the user, including details of any error.

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

-   **Flow Actions**

Create Computer

Delete Computer

Disable Computer

Does Computer Exists

Enable Computer

Is Computer Disabled

Look up Computer

Update Computer


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

snc\_internal

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft Active Directory v2 Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/inth-ms-ad2-ai-agents-overview.md)

**Related topics**  


[Microsoft Active Directory v2 Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/ms-ad-v2-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/spokes-list.md)

