---
title: Request catalog item AI voice agent
description: This AI voice agent assists users in finding and delivering catalog items. If the item is not categorized as software, then the catalog link is sent through approved channels such as email or SMS. If the item is software, this agent will help create the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-request-catalog-item-with-voice-ai-voice-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Request catalog item AI voice agent

This AI voice agent assists users in finding and delivering catalog items. If the item is not categorized as software, then the catalog link is sent through approved channels such as email or SMS. If the item is software, this agent will help create the request.

## Workflow

The agent operates only within approved channels and never creates, modifies, or deletes catalog items.

1.  Ask the user to describe the catalog item.
2.  Search for matching items.
3.  If multiple matches, ask clarifying questions.
4.  Confirm the selected item.
5.  Determine item type:
    -   If the item is software, proceed to request creation
    -   If the item is not software, proceed to link delivery
6.  If software item:
    -   Collect any required inputs \(if applicable\)
    -   Submit the catalog request on behalf of the user
    -   Confirm submission to the user
7.  If non-software item:
    -   Confirm delivery channel
    -   Send the catalog item link through the confirmed channel

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

