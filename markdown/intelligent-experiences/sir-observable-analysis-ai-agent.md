---
title: Observable analysis AI agent
description: This Operational Technology Security Incident Response agent performs threat lookups, observable enrichment, sighting searches, and block requests against observables in a security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sir-observable-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Security Incident Response AI agents, Security Incident Response, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Observable analysis AI agent

This Operational Technology Security Incident Response agent performs threat lookups, observable enrichment, sighting searches, and block requests against observables in a security incident.

## Workflow

1.  Retrieve the incident's observables \(URLs, IPs, file hashes, email addresses, etc.\). Run threat lookup, observable enrichment, or both as requested. Wait for the user to confirm that the capability execution is complete before fetching and displaying results.
2.  Retrieve observables and run a sighting search to find internal and external sighting information. If the search times out, retrieve results after the user manually confirms completion.
3.  Retrieve observables identified as malicious. If none exist, inform the user and stop. Run the block request and wait for user confirmation that execution is complete.

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

Fetch observables associated to security incident

Retrieve capability execution results

Run block request

Run observable enrichment

Run threat lookup

-   **Subflow**

Run sighting search tool


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

