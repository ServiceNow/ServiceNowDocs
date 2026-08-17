---
title: CBS Bulk Upload AI Agent
description: The CBS Bulk Upload AI agent handles bulk record creation and updates for the Space, Supplier, and Supplier Contact tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cbs-cbs-bulk-upload-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Core Business Suite AI agents, Core Business Suite, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# CBS Bulk Upload AI Agent

The CBS Bulk Upload AI agent handles bulk record creation and updates for the Space, Supplier, and Supplier Contact tables.

## Workflow

The agent helps users complete tasks related to Core Business Suite bulk upload.

1.  Agent informs user that it will help them upload via a guided process.
2.  Select the appropriate table based on user input.
3.  Prepare template for data upload and present to user for modifications.
4.  User uploads file.
5.  Validate the file.
6.  If no errors, import the data.
7.  Display completion summary.

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

Agent Context Retriever

Copy the Attachment to Data Source Record

Get Import Set Record Link

Get Records Count

Get Template Attachment Link for Bulk Edit

Get Template Attachment Link for Bulk Upload

Get Validations

Run Scheduled Data Import

Update agent result

-   **Conversational topics \(Virtual Agent\)**

Submit and Fetch Results

Upload Updated Template


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ia\_config.ia\_user, import\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ia\_config.ia\_user, import\_admin, platform\_ml\_di.creation\_agent

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
</table>Learn more about Core Business Suite at [Core Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/cbs-landing.md).

**Parent Topic:**[Core Business Suite AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cbs-ai-agents-overview.md)

