---
title: Security incident wrap up generator AI agent
description: This Operational Technology Security Incident Response agent can close a security incident by performing all pre-closure validations. It can also generate close notes, generate post incident analysis, post work note, and update the state of the security incident to close it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sir-security-incident-wrap-up-generator-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Security Incident Response AI agents, Security Incident Response, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Security incident wrap up generator AI agent

This Operational Technology Security Incident Response agent can close a security incident by performing all pre-closure validations. It can also generate close notes, generate post incident analysis, post work note, and update the state of the security incident to close it.

## Workflow

1.  If the user explicitly requests closing as a false positive, follow the short path. Otherwise, follow the full closure path.
2.  Retrieve the incident details. If already closed or cancelled, inform the user and end.
3.  If the user explicitly requests closing as a false positive, close the incident immediately and end.
4.  If the user doesn't explicitly requests closing as a false positive, warn the user if open response tasks or mandatory assessments will be affected. Get approval before continuing.
5.  Produce a post-incident analysis, close notes, and a suggested close code. The user reviews and approves or revises each before proceeding.
6.  Write the approved content to the record and confirm closure.

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

Close security incident as false positive

Fetch security incident details

Generate close notes for security incident

Generate post incident analysis for security incident

Update security incident closure information


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_si.analyst

</td></tr><tr><td>

Data access roles

</td><td>

sn\_si.analyst

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

Wrap up security incident

</td></tr></tbody>
</table>Learn more about Operational Technology Security Incident Response at .

**Parent Topic:**[Security Incident Response AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sir-ai-agents-overview.md)

