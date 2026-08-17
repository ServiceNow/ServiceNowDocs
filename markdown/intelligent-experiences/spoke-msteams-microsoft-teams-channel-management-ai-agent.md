---
title: Microsoft Teams channel management AI agent
description: This Microsoft Teams integration agent manages Microsoft Teams channels through ServiceNow Integration Hub. This agent can create channels, manage members, and retrieve channel information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spoke-msteams-microsoft-teams-channel-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Integration Hub AI agents, Integration Hub, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Microsoft Teams channel management AI agent

This Microsoft Teams integration agent manages Microsoft Teams channels through ServiceNow Integration Hub. This agent can create channels, manage members, and retrieve channel information.

## Workflow

1.  Identify which channel management operation the user needs from the eight supported actions.
2.  Gather the necessary parameters and perform the operation. Supported actions are:
    -   **Lookup**

        Retrieve channel details by ID or name, list all channels, or list channel members.

    -   **Create or Delete**

        Create or delete a channel.

    -   **Membership**

        Add or remove members from a channel.


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

-   **Flow Actions**

Add member to channel

Create channel

Delete channel

Look up channel

Look up channel by name

Look up channel members

Look up channels

Remove member from channel


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

snc\_internal

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
</table>Learn more about Integration Hub at [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub.md).

**Parent Topic:**[Integration Hub AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrationhub-ai-agents-overview.md)

