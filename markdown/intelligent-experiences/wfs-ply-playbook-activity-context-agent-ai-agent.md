---
title: Playbook activity context AI agent
description: This ServiceNow Otto for Creator agent helps users complete ServiceNow forms by fetching form fields, automatically matching pre-filled field values, and prompting for any missing required information. The agent saves the summary of what it has done.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wfs-ply-playbook-activity-context-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Creator AI agents, ServiceNow Otto for Creator, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Playbook activity context AI agent

This ServiceNow Otto for Creator agent helps users complete ServiceNow forms by fetching form fields, automatically matching pre-filled field values, and prompting for any missing required information. The agent saves the summary of what it has done.

## Workflow

1.  Pull the form's field definitions \(formFields\), including each field's type, label, constraints, and reference/choice details.
2.  Extract the most relevant available data for each field, matching field type. Leave fields empty when no relevant data exists rather than guessing.
3.  Compress or truncate any value that exceeds its field's character limit before assigning it.
4.  Package all filled fields into the required schema, along with a summary of the activity and separate success/failure variants of that summary.
5.  Execute the slot-filling script with the completed fields and summary.
6.  If the JSON output is malformed \(not if data is simply missing or wrong\), regenerate it one time; otherwise accept the result as final.

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

Playbook Slot Filling Script


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

playbook.agent\_user

</td></tr><tr><td>

Data access roles

</td><td>

Not defined.

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

Playbook Activity Assist

</td></tr></tbody>
</table>Learn more about ServiceNow Otto for Creator at [ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator-landing.md).

**Parent Topic:**[ServiceNow Otto for Creator AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-creator-ai-agents-overview.md)

