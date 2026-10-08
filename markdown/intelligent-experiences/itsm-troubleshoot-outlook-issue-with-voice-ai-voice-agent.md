---
title: Troubleshoot Outlook issue AI voice agent
description: This AI voice agent troubleshoots Microsoft Outlook issues. It also sends a troubleshooting article link to the user by email when requested.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-troubleshoot-outlook-issue-with-voice-ai-voice-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Troubleshoot Outlook issue AI voice agent

This AI voice agent troubleshoots Microsoft Outlook issues. It also sends a troubleshooting article link to the user by email when requested.

## Workflow

1.  Greet the user and ask them if they need any help with Microsoft Outlook.
2.  Fetch the KB articles related to user query and answer in a concise manner
3.  Use the KB articles to answer the follow up questions.
4.  If you are unable to answer any question, offer to transfer to an agent.
5.  If they are satisfied and want no more details, politely end the conversation. If they are not satisfied, offer to transfer to an agent.
6.  If they want to be transferred, do so and end the conversation.
7.  If there are multiple steps, give each step one at a time and wait for the user to confirm they are ready for the next step.

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

