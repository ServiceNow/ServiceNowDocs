---
title: Exchange online integration handling AI agent
description: This Operational Technology Security Incident Response agent searches for and deletes emails related to a security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sir-exchange-online-integration-handling-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Security Incident Response AI agents, Security Incident Response, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Exchange online integration handling AI agent

This Operational Technology Security Incident Response agent searches for and deletes emails related to a security incident.

## Workflow

1.  Run an email search based on the incident context. If no search criteria exist, ask the user how to proceed. Wait for user confirmation that the search is complete before fetching results.
2.  Only available after a search has been performed. If the search returned no emails, stop. Otherwise, run the deletion, wait for user confirmation that it is complete, and fetch results.

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

Delete email from server

Fetch email deletion results

Fetch email search results

Search email on server


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

