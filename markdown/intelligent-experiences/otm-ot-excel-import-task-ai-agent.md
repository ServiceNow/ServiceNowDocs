---
title: OT Excel import task AI agent
description: The OT Excel import task AI agent imports Operational Technology \(OT\) device data from a spreadsheet into the Configuration Management Database \(CMDB\). The agent validates the imported records, creates remediation tasks for invalid records, and imports the valid records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/otm-ot-excel-import-task-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [Operational Technology Manager AI agents, Operational Technology Manager \(OTM\), AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# OT Excel import task AI agent

The OT Excel import task AI agent imports Operational Technology \(OT\) device data from a spreadsheet into the Configuration Management Database \(CMDB\). The agent validates the imported records, creates remediation tasks for invalid records, and imports the valid records.

## Workflow

The agent helps the user import OT devices from a spreadsheet into the CMDB.

1.  Create an OT Excel import task record and share a link to it with the user.
2.  Ask the user to attach a spreadsheet of OT device data to the import task record, using the template available in the **Attachments** panel as a guide.
3.  After the user confirms the spreadsheet is attached, process it into the SG OT Excel Stagings table.
4.  Share any failure messages so that the user can correct and re-upload the spreadsheet.
5.  Ask the user to wait until the import task state changes to **Staging import succeeded**.
6.  After the user confirms, validate the staged records and report how many are valid, partially valid, and invalid.
7.  If any records are invalid, offer to create remediation tasks for them.
8.  If any records are valid or partially valid, ask whether to import them into the CMDB, and start the import if the user confirms.
9.  Tell the user that the import runs in the background and that the task state changes to CMDB import complete when it finishes.

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

-   **Script**

\[AIA Tool\] CMDB Importer

\[AIA Tool\] Excel Sheet Importer

\[AIA Tool\] Import Task Link Generator

\[AIA Tool\] Remediation Task Creator

\[AIA Tool\] Staging Validator


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Not defined.

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

Import OT device spreadsheet into OT CMDB

</td></tr></tbody>
</table>**Parent Topic:**[Operational Technology Manager AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/otm-ai-agents-overview.md)

