---
title: Triage cases planner AI agent
description: This AI agent triages cases. It takes appropriate actions based on the record's sentiment and intents. It is intended for agents and end-users who need assistance in resolving queries efficiently, as well as assessing a record for possible case creation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-triage-cases-planner-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Triage cases planner AI agent

This AI agent triages cases. It takes appropriate actions based on the record's sentiment and intents. It is intended for agents and end-users who need assistance in resolving queries efficiently, as well as assessing a record for possible case creation.

## Workflow

The agent helps users complete tasks related to triage cases planner.

1.  Invoke the context validator AI agent to validate the record.
2.  If the sentiment is negative, use the case creation AI agent to create a case. If the sentiment is neutral or positive, proceed to step 3.
3.  Invoke the informational queries AI agent to process informational intents.
4.  Invoke the transactional queries AI agent to process the list of transactional intents.
5.  Invoke the case creation AI agent from the team to create the case.
6.  Generate a customer reply.
7.  Invoke the email response AI agent to generate and send an email response.
8.  Generate the execution overview and add it to the case work notes.

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

Generate Customer Reply Content

Get list of intent of specific type

-   **Flow Action**

Update source record worknotes


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_esm\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_esm\_agent

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
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md).

**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/csm-ai-agents-overview.md)

