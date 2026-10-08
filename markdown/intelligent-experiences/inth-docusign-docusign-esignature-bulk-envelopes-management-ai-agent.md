---
title: Docusign eSignature bulk envelopes management AI agent
description: This AI agent manages Docusign eSignature bulk sending. It creates, updates, looks up, and deletes bulk send lists, creates bulk send and test requests, and looks up and updates bulk send batches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-docusign-docusign-esignature-bulk-envelopes-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [Docusign eSignature Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Docusign eSignature bulk envelopes management AI agent

This AI agent manages Docusign eSignature bulk sending. It creates, updates, looks up, and deletes bulk send lists, creates bulk send and test requests, and looks up and updates bulk send batches.

## Workflow

The agent helps the user send envelopes in bulk with Docusign eSignature.

1.  Ask the user what they want to do and collect the details the action needs, such as the bulk send list or batch ID.
2.  Look up bulk send lists or a specific list.
3.  Create, update, or delete a bulk send list.
4.  Create a bulk send test request or a bulk send request.
5.  Look up bulk send batches, their envelopes, or a batch's status.
6.  Update a batch's status or apply a batch action.
7.  Report the outcome to the user, including details of any error.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Actions**

Create Bulk Send List

Create Bulk Send Request

Create Bulk Send Test Request

Delete Bulk Send List

Look up Bulk Send Batch Envelopes Stream

Look up Bulk Send Batch Status

Look up Bulk Send Batches Stream

Look up Bulk Send List

Look up Bulk Send Lists

Update Bulk Send Batch Action

Update Bulk Send Batch Status

Update Bulk Send List


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Docusign eSignature Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-docusign-ai-agents-overview.md)

**Related topics**  


[Docusign eSignature Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/docusign-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

