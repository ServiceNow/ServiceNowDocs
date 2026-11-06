---
title: CMDB data model navigator AI agent
description: Answers questions about the CMDB data model, including classes, tables, fields, and relationships, by using the CMDB data model navigator capability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/cmdb-cmdb-data-model-navigator-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-14"
reading_time_minutes: 1
breadcrumb: [CMDB AI agents, CMDB, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# CMDB data model navigator AI agent

Answers questions about the CMDB data model, including classes, tables, fields, and relationships, by using the CMDB data model navigator capability.

## Workflow

This agent responds to questions about how configuration items are structured and related in the CMDB data model. For more information, see [Data model navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/na-cmdb-awf-data-model-navigator.md).

1.  Receive the question about the data model.
2.  Retrieve the matching classes, tables, fields, and relationships.
3.  Return the information in response to the original question.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Capability**

CMDB Data Model Navigator


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_cmdb\_user, sn\_data\_model\_nav.data\_model\_navigator\_read

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_cmdb\_user, sn\_data\_model\_nav.data\_model\_navigator\_read

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

CMDB Data Model Navigator Assistant

</td></tr></tbody>
</table>Learn more about Configuration Management Database \(CMDB\) at [Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_ITILConfigurationManagement.md).

**Parent Topic:**[CMDB AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cmdb-ai-agents-overview.md)

