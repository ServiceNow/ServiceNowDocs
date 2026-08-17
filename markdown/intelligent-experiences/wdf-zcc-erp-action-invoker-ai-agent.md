---
title: ERP action invoker AI agent
description: This Workflow Data Fabric agent assists in gathering user inputs for a specific operation. It generates mandatory and optional inputs, and presents them to the user in a form. The user can then supply values for the mandatory inputs, and the agent formats and pass these inputs to a tool to invoke an action script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wdf-zcc-erp-action-invoker-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Workflow Data Fabric AI agents, Workflow Data Fabric AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# ERP action invoker AI agent

This Workflow Data Fabric agent assists in gathering user inputs for a specific operation. It generates mandatory and optional inputs, and presents them to the user in a form. The user can then supply values for the mandatory inputs, and the agent formats and pass these inputs to a tool to invoke an action script.

## Workflow

1.  Pull the model ID and operation ID from the provided JSON.
2.  Check the validation strategy for mandatory fields. Ask for just one, all, or whether the user wants to provide any at all, depending on the strategy type.
3.  Request all needed mandatory fields at once, in a single consolidated response.
4.  Ask whether to include optional fields. If so, show the full optional fields list once and collect all desired values together.
5.  Pass the collected inputs along with the model ID and operation ID to run the action.
6.  After execution, show a fixed notice that results are capped at 10 records and truncated beyond that.

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

Invoke ERP Action

Retrieve Mandatory and Optional Inputs


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Explore ERP models

</td></tr></tbody>
</table>Learn more about Workflow Data Fabric at [Build an automation with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/build-automation-now-assist.md).

**Parent Topic:**[Workflow Data Fabric AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/wdf-ai-agents-overview.md)

