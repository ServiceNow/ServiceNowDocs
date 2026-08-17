---
title: Spend categorization AI agent
description: This Sourcing and Procurement Operations agent predicts and populates product and spend categories in purchase requisition lines, reducing manual effort and improving data accuracy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spo-spend-categorization-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Sourcing and Procurement Operations AI agents, Sourcing and Procurement Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Spend categorization AI agent

This Sourcing and Procurement Operations agent predicts and populates product and spend categories in purchase requisition lines, reducing manual effort and improving data accuracy.

## Workflow

1.  Run category prediction and document extraction based on user provided ID
2.  Identify whether the user wants to update product categories or spend categories.
3.  Extract purchase header record numbers from the user's request, and optionally collect a reason for the update and a suggested category.
4.  Run the validation tool to generate AI-suggested categories and present both AI and user suggestions as selectable options.
5.  Let the user choose a category for each line item or skip individual lines.
6.  Submit the selected categories to update the records.

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

Category prediction

Document extraction

Spend category validation

Update record


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_shop.procurement\_specialist, sn\_spend\_gen\_ai.now\_assist\_fulfiller

</td></tr><tr><td>

Data access roles

</td><td>

sn\_shop.procurement\_specialist, sn\_spend\_gen\_ai.now\_assist\_fulfiller

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
</table>Learn more about Sourcing and Procurement Operations at [Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/psm-overview.md).

**Parent Topic:**[Sourcing and Procurement Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/spo-ai-agents-overview.md)

