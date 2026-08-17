---
title: Release lifecycle documentation AI agent
description: Generate business release notes in natural, human-friendly language for business stakeholders, within a maximum 4000 character limit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aemc-release-lifecycle-documentation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [App Engine Management Center AI agents, App Engine Management Center \(AEMC\), Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Release lifecycle documentation AI agent

Generate business release notes in natural, human-friendly language for business stakeholders, within a maximum 4000 character limit.

## Workflow

The agent helps users complete tasks related to release lifecycle documentation.

1.  Receive the user's request and validate required inputs.
2.  Execute the appropriate tools to perform the requested action.
3.  Return the results or update the relevant record.

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

-   **Topic Block**

Release Notes Generator


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

update\_set\_admin

</td></tr><tr><td>

Data access roles

</td><td>

update\_set\_admin, 7edf53c0ff3132101bfbffffffffffcc

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
</table>Learn more about at App Engine Management Center at [App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center.md).

**Parent Topic:**[App Engine Management Center AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aemc-ai-agents-overview.md)

