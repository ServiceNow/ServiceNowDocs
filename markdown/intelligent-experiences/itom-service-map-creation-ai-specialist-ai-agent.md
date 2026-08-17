---
title: Service map creation AI specialist
description: This AI specialist discovers service infrastructure from application service candidates using ML analysis, and then it maps and persists the full service topology in CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-service-map-creation-ai-specialist-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Service map creation AI specialist

This AI specialist discovers service infrastructure from application service candidates using ML analysis, and then it maps and persists the full service topology in CMDB.

## Workflow

The agent helps users complete tasks related to service map creation ai specialist.

1.  Call the Get ML Candidate Full Data tool with the candidate number from the objective. This returns candidate sys\_id, candidate name, server list with host names, and IPs.
2.  Call the Get Candidate Running Processes tool with the same candidate number. This returns the running process details, AFP groups, connection data, and key ports.
3.  Determine the suggested\_name: a concise, business-meaningful service name derived from the identified technology.
4.  Create and save the service topology.
5.  Inform the user of all changes.

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

create\_service\_topology

Get Candidate Running Processes

Get ML Candidate Full Data

Save Candidate Analysis

save\_run\_record


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

service\_mapping\_ai\_user, cmdb\_read, itom\_admin, snc\_internal, snc\_required\_script\_writer\_permission, sn\_bm\_client.benchmark\_data\_viewer, sn\_itom\_license.reader

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
</table>Learn more about IT Operations Management at [IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/r_ITOMApplications.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

