---
title: Workflow data fabric product recommendation AI agent
description: This Workflow Data Fabric agent evaluates integration requirements, data movement needs, communication flows, and automation objectives expressed in the user's prompt and determines the most suitable workflow data fabric product.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wdf-workflow-data-fabric-product-recommendation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Workflow Data Fabric AI agents, Workflow Data Fabric AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Workflow data fabric product recommendation AI agent

This Workflow Data Fabric agent evaluates integration requirements, data movement needs, communication flows, and automation objectives expressed in the user's prompt and determines the most suitable workflow data fabric product.

## Workflow

1.  Check whether the user has specified a source/target system and an integration objective or pattern, clarifying with targeted questions if needed.
2.  Search the internal knowledge base.
3.  Identify a best-fit product plus up to two alternatives, with rationale and trade-offs for each.
4.  Always show visible output: either a specific recommendation with alternatives, or \(if context was insufficient\) a general product list suggesting the user consult documentation or a solutions architect.

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

-   **Search retrieval**

Internal KB Recommendations


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

connection\_admin, wdf\_operator, maint, df\_data\_steward, wdf\_consumer, wdf\_builder

</td></tr><tr><td>

Data access roles

</td><td>

wdf\_builder, wdf\_consumer, wdf\_operator, df\_data\_steward, connection\_admin

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

