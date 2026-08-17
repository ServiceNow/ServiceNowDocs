---
title: Security incident resolution AI agent
description: This Operational Technology Security Incident Response agent walks the user through resolving a security incident by generating and executing a resolution plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sir-security-incident-resolution-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Security Incident Response AI agents, Security Incident Response, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Security incident resolution AI agent

This Operational Technology Security Incident Response agent walks the user through resolving a security incident by generating and executing a resolution plan.

## Workflow

1.  Fetch the security incident details and resolution plan. End if already closed or resolved.
2.  Summarize the incident's current state, including any resolution steps already completed, and show it to the user.
3.  Present the resolution plan for user review. Iterate on revisions until the user approves.
4.  Execute each step in the approved plan in order. Falls back to other agents for steps it can't perform itself.
5.  Confirm completion with the user. Only end when the user explicitly confirms no further actions are needed.

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

-   **Script**

Fetch security incident details and resolution steps


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

Resolve security incident

</td></tr></tbody>
</table>Learn more about Operational Technology Security Incident Response at .

**Parent Topic:**[Security Incident Response AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sir-ai-agents-overview.md)

