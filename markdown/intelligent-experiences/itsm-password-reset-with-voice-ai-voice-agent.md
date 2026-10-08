---
title: Password reset AI voice agent
description: This AI voice agent helps users reset their password during phone-based interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-password-reset-with-voice-ai-voice-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Password reset AI voice agent

This AI voice agent helps users reset their password during phone-based interactions.

## Workflow

The agent sends a password reset link through email or SMS to ensure a successful reset.

1.  Ensure you have the name of the password reset application. If not provided, ask the user to describe or name the application.
2.  Call the application search tool with the provided name to retrieve possible matches.
3.  If the tool returns multiple matches, ask clarifying questions.
4.  Confirm the selected application and explicitly ask for the delivery method.
5.  Send or read out the password reset link based on the confirmed method.

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

public

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

