---
title: Document verification AI agent
description: The document verification AI agent verifies the documents on a record to determine if they match the documents listed for the case type. Additionally, they determine if any documents are missing or if document verification has failed. This agent should be invoked when documents need to be verified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-document-verification-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Document verification AI agent

The document verification AI agent verifies the documents on a record to determine if they match the documents listed for the case type. Additionally, they determine if any documents are missing or if document verification has failed. This agent should be invoked when documents need to be verified.

## Workflow

The agent helps users complete tasks related to document verification.

1.  Get the source record details.
2.  Get the case type.
3.  Get the list of required documents.
4.  Initiate the document verification.
5.  Perform the document verification.
6.  Compare the valid documents and the list of required documents.
7.  Save the list of missing required documents.
8.  Communicate to the user the document validation outcome.

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

Get Required Documents List

Initiate Document Verification

Record the results of the document validation process

Save the list of missing required documents

-   **Subflow**

Verify the documents


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

