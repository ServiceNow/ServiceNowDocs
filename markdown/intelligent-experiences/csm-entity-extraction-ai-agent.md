---
title: Entity extraction AI agent
description: The entity extraction AI agent extracts entities from emails and information from documents. It matches the entities with a list of approved fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-entity-extraction-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Entity extraction AI agent

The entity extraction AI agent extracts entities from emails and information from documents. It matches the entities with a list of approved fields.

## Workflow

1.  Get the source record details.
2.  Get the case type.
3.  Get the operation type.
4.  Identify entity extracted fields.
5.  Check for task definition ID for document extraction.
6.  Perform document extraction.
7.  Update the record with the final fields to update.
8.  Communicate the final fields to update to the user.

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

Get record details

Identify entity extracted fields

Update record fields

-   **Subflows**

Perform Document Extraction


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_esm\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_customerservice\_manager

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

Triage cases

</td></tr></tbody>
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md).

**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/csm-ai-agents-overview.md)

