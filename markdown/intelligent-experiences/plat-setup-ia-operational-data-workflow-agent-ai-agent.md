---
title: IA operational data workflow AI agent
description: This ServiceNow Otto for Setup AI agent automates the configuration of data imports by handling the creation of data sources, import sets, and transform maps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-setup-ia-operational-data-workflow-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Setup Hub AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# IA operational data workflow AI agent

This ServiceNow Otto for Setup AI agent automates the configuration of data imports by handling the creation of data sources, import sets, and transform maps.

## Workflow

The agent is designed for IT administrators and system integrators.

1.  Retrieve and parse execution context.
2.  Check user role authorization for the table.
3.  Determine the source selection.
4.  Display recommended fields.
5.  Upload and validate the file.
6.  Import the file.

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

Agent Context Retriever

Cache Transform Map Ref

Check Has Role

Check If Map Has Coalesce

Get Import Config

Incomplete Data Imports

Orchestrator Execution Manager

Process Import

Transform Import Set

Update Coalesce Field

-   **Generative AI skill**

IA Operational Data Coalesce Skill

-   **Conversational topics**

IAFileUploadAndValidator

IAPreviewTransformMapView


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

user\_admin, import\_admin, sn\_ia\_config.ia\_user, sn\_aia.viewer

</td></tr><tr><td>

Data access roles

</td><td>

user\_admin, import\_admin, sn\_aia.viewer

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

Not applicable.

</td></tr></tbody>
</table>Learn more about ServiceNow Otto for Setup at [ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-landing.md).

**Parent Topic:**[Setup Hub AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-setup-ai-agents-overview.md)

