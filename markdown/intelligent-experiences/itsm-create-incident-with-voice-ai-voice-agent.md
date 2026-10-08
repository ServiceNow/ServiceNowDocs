---
title: Create incident AI voice agent
description: This AI agent creates new incidents when the user explicitly mentions they want to create a new incident or report a new issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/itsm-create-incident-with-voice-ai-voice-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI assets, Enable AI experiences]
---

# Create incident AI voice agent

This AI agent creates new incidents when the user explicitly mentions they want to create a new incident or report a new issue.

## Workflow

1.  Check whether the caller already stated their issue during the initial routing or transfer.
2.  If more context would help, ask up to two follow-up questions \(one at a time\).
3.  Summarize the issue in one sentence and briefly state any follow-up answers received.
4.  Create the incident and read the incident number back to the user and inform them they will receive an email with the details.
5.  After confirming the incident number, say: "Is there anything else you'd like help with?"

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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itsm-ai-agents-overview.md)

