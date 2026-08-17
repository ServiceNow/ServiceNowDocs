---
title: Security incident shift handover AI agent
description: This Operational Technology Security Incident Response agent adds a security incident to a shift handover report, walking the user through each section for review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sir-security-incident-shift-handover-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Security Incident Response AI agents, Security Incident Response, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Security incident shift handover AI agent

This Operational Technology Security Incident Response agent adds a security incident to a shift handover report, walking the user through each section for review.

## Workflow

1.  Get a valid security incident number from the user if one is not provided.
2.  Run the pre-processor to find active shift handover records for the user. If none exist, inform the user and end.
3.  If multiple shift handover records exist, ask the user to select one.
4.  Validate the selected handover record and generate its content. If validation fails, ask for a valid record number.
5.  If the security incident is already in the report, inform the user and get confirmation before adding it again.
6.  Walk through each section of the report. For each section, show the content, collect approval or revisions, and save to the database before moving to the next section.
7.  After all sections are processed, show a summary of saved and skipped sections.

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

Pre-processor for shift handover

Save section content to database

Validate and generate shift handover content


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_si.manager, sn\_si.analyst

</td></tr><tr><td>

Data access roles

</td><td>

sn\_si.basic, sn\_escm\_sh.shift\_analyst

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

Generate SIR Shift Handover Report

</td></tr></tbody>
</table>Learn more about Operational Technology Security Incident Response at .

**Parent Topic:**[Security Incident Response AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sir-ai-agents-overview.md)

