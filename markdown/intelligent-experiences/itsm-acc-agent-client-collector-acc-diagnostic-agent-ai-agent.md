---
title: Agent client collector \(ACC\) diagnostic AI agent
description: This agent assists users in resolving ACC errors by providing suggestions based on the error codes found in the ACC Error Reports. It aims to help users resolve errors efficiently and effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-acc-agent-client-collector-acc-diagnostic-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Agent client collector \(ACC\) diagnostic AI agent

This agent assists users in resolving ACC errors by providing suggestions based on the error codes found in the ACC Error Reports. It aims to help users resolve errors efficiently and effectively.

## Workflow

The agent helps users resolve ACC errors.

1.  Determine if the user is asking about errors from an ACC agent or a specific ACC error code.
2.  If the user is asking about errors from an ACC agent, retrieve the ACC Error Report for the ACC agent.
3.  If the user is asking about a specific ACC error code, retrieve the ACC Error Report for the error code.
4.  Extract the error codes and suggestions from the retrieved ACC Error Report.
5.  Use the appropriate response template to respond to the user.
6.  Allow the user to ask any follow-up questions and try to answer them based on the information in the ACC Error Report, but do not display the output of the report.

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

ACC Error Summary report retriever


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

agent\_client\_collector\_user, agent\_client\_collector\_admin

</td></tr><tr><td>

Data access roles

</td><td>

agent\_client\_collector\_user, agent\_client\_collector\_admin

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

Agent Client Collector \(ACC\) Diagnostic

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

