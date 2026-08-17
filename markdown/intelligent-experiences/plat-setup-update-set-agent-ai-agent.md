---
title: Update set AI agent
description: This ServiceNow Otto for Setup AI agent helps administrators and developers upload, review, and commit XML update sets efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-setup-update-set-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Setup Hub AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Update set AI agent

This ServiceNow Otto for Setup AI agent helps administrators and developers upload, review, and commit XML update sets efficiently.

## Workflow

1.  Outline the steps that will run \(upload, validate, retrieve, preview, conflict handling, commit\) and wait for the user to confirm before starting.
2.  Accept the XML file upload and retrieve its attachment details.
3.  Check the uploaded file is a valid update set XML.
4.  Pull the validated update set into the instance.
5.  Run a preview to detect conflicts with existing configuration.
6.  If conflicts exist, let the user review errors, then accept all, reject all, or resolve manually before rechecking.
7.  Commit the update set and confirm success, or report a failure with retry/stop options.

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

Accept All Updates from Remote

Check Update Set Commit

Commit Update Set

Get Attachment Details from record

Get Preview Error Link

Preview Update Set

Reject All Updates from Remote

Retrieve Update Set

Validate Update Set

-   **Conversational topic**

Upload xml


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ia\_config.ia\_user

</td></tr><tr><td>

Data access roles

</td><td>

admin

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
</table>Learn more about ServiceNow Otto for Setup at [ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-landing.md).

**Parent Topic:**[Setup Hub AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-setup-ai-agents-overview.md)

