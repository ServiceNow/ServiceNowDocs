---
title: CI form contextual help AI agent
description: CI form contextual help AI agent helps users by answering questions about CI attributes and classes. It guides them through CI forms, dashboards, home pages, and other views on the workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cmdb-ci-form-contextual-help-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [CMDB AI agents, CMDB, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# CI form contextual help AI agent

CI form contextual help AI agent helps users by answering questions about CI attributes and classes. It guides them through CI forms, dashboards, home pages, and other views on the workspace.

## Workflow

The agent helps users complete tasks related to CI form contextual help.

1.  Greet user or ask if they want to continue a previous conversation.
2.  Perform search and answer user questions.
3.  Close conversation only if user indicates they are completely done.

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

Get Page Context

-   **Generative AI skill**

Search product documentation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_cmdb\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_cmdb\_user

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

Show contextual CI form help

</td></tr></tbody>
</table>Learn more about Configuration Management Database \(CMDB\) at [Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_ITILConfigurationManagement.md).

**Parent Topic:**[CMDB AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cmdb-ai-agents-overview.md)

