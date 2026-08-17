---
title: Workflow data fabric flow generation AI agent
description: This Workflow Data Fabric agent transforms a user's natural-language integration intent into a generated Workflow Studio flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wdf-workflow-data-fabric-flow-generation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Workflow Data Fabric AI agents, Workflow Data Fabric AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Workflow data fabric flow generation AI agent

This Workflow Data Fabric agent transforms a user's natural-language integration intent into a generated Workflow Studio flow.

## Workflow

1.  Get the target application scope from the user \(required\).
2.  Determine what the user wants the flow to do, checking whether the trigger and actions are both clear enough to proceed.
3.  If trigger or action details are too vague, ask 1-2 targeted questions.
4.  Build an imperative prompt from the user's intent, derive a name and description, invoke the generation tool once, and return the Workflow Studio link exactly as provided.
5.  If generation isn't possible, provide a direct link to Workflow Studio with context about what went wrong.

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

Check Flow Generation Skill

Check User Flow Permissions

Generate Flow From Intent

Generate Workflow Studio Link

Look up Scope


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

wdf\_builder, maint, wdf\_operator

</td></tr><tr><td>

Data access roles

</td><td>

wdf\_builder, wdf\_operator

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

Default VA Workflow

</td></tr></tbody>
</table>Learn more about Workflow Data Fabric at [Build an automation with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/build-automation-now-assist.md).

**Parent Topic:**[Workflow Data Fabric AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/wdf-ai-agents-overview.md)

