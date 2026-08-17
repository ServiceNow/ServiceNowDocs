---
title: VR data retrieval agent AI agent
description: This Unified Security Exposure Management agent answers questions about vulnerability response data by constructing and executing table queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/usem-data-retrieval-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Unified Security Exposure Management AI agents, Unified Security Exposure Management AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# VR data retrieval agent AI agent

This Unified Security Exposure Management agent answers questions about vulnerability response data by constructing and executing table queries.

## Workflow

1.  Introduce the agent's capabilities with example queries and ask how to help.
2.  Prompt for a request, ask for clarification if anything is ambiguous or incomplete, and redirect if the request falls outside Vulnerability Response scope.
3.  Call the search tool and return its response exactly as received.
4.  Ask if the user wants to refine the query or run another search.
5.  Continue the loop until the user says they're finished.

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

Search tool


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_vul.remediation\_owner, sn\_vul.app\_sec\_manager, sn\_vul.vulnerability\_admin, sn\_vul.vulnerability\_analyst

</td></tr><tr><td>

Data access roles

</td><td>

sn\_vul.remediation\_owner, sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, sn\_vul.app\_sec\_manager

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

Retrieve VR data

</td></tr></tbody>
</table>Learn more about Unified Security Exposure Management at [Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/unified-security-exposure-management-landing-page.md).

**Parent Topic:**[Unified Security Exposure Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/usem-ai-agents-overview.md)

