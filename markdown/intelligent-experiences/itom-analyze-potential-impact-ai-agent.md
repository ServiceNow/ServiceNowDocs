---
title: Analyze potential impact AI agent
description: This agent analyzes the potential business and operational impact of a proposed change by identifying affected servers and services. The agent reviews the change request, performs impact analysis, and documents findings in work notes to support informed decision-making and effective mitigation strategies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-analyze-potential-impact-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Analyze potential impact AI agent

This agent analyzes the potential business and operational impact of a proposed change by identifying affected servers and services. The agent reviews the change request, performs impact analysis, and documents findings in work notes to support informed decision-making and effective mitigation strategies.

## Workflow

The agent analyzes a change request to identify and document the potential impact on services and servers.

1.  Validate that all prerequisites for the impact analysis are met before proceeding.
2.  Extract the affected server IDs from the change request.
3.  Identify which services are potentially impacted by mapping affected servers to suggested services.
4.  Retrieve a combined view of impacted servers and suggested services.
5.  Perform a full impact analysis for each suggested service, including cascading effects.
6.  Compile the analysis results and update the change request work notes with a consolidated summary.

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

Analyze potential impact prerequisites validator

Extract Data from Change Request

Get Impacting Servers Per Suggested Service

Update Change Request Work Notes

-   **Flow Actions**

Get Full Impact Analysis of Each Suggested Service

Get Impacted Servers and Suggested Services


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_change\_write

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

Analyze Potential Impact

</td></tr></tbody>
</table>Learn more about IT Operations Management at [IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/r_ITOMApplications.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

