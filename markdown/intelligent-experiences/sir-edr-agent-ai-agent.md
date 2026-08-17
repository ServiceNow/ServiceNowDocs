---
title: EDR AI agent
description: This Operational Technology Security Incident Response agent retrieves host details or isolates a host associated with a security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sir-edr-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Security Incident Response AI agents, Security Incident Response, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# EDR AI agent

This Operational Technology Security Incident Response agent retrieves host details or isolates a host associated with a security incident.

## Workflow

1.  Identify the configuration item \(CI\) from the security incident using hostname, IP address, or device identifier. If no CI is found, inform the user and stop. Run the get host details action. If the request fails, inform the user and stop.
2.  Identify the CI and security incident from user input. If no CI is found, ask the user how to proceed. Run the isolate host action. If the request fails, ask the user how to proceed.

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

-   **Subflows**

Isolate host

Run get host details tool


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

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Resolve security incident

</td></tr></tbody>
</table>Learn more about Operational Technology Security Incident Response at .

**Parent Topic:**[Security Incident Response AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sir-ai-agents-overview.md)

