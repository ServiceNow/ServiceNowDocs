---
title: Software reclamation rule creation AI agent
description: This Software Asset Management agent analyzes software utilization and spend, then creates a reclamation rule based on user-approved criteria.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sam-software-reclamation-rule-creation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Software Asset Management AI agents, Software Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Software reclamation rule creation AI agent

This Software Asset Management agent analyzes software utilization and spend, then creates a reclamation rule based on user-approved criteria.

## Workflow

1.  Identify the target product. If a Product ID is provided, use it directly. Otherwise, present available products for the user to select.
2.  Fetch reclamation rule suggestions for the product. If a rule already exists, show the user a link to it and end.
3.  Analyze utilization and spend data, then present the analysis alongside a draft reclamation rule for user review.
4.  Collect feedback. The user can approve the draft, request changes \(including reclamation type, thresholds, and other rule details\), or cancel. Iterate until approved or cancelled.
5.  Create the reclamation rule using the approved details.
6.  If other existing reclamation rules lack a VIP exclusion condition, offer to update them. Only update if the user approves.
7.  If software usage data collection is not set up, notify the user with a documentation link.

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

Create reclamation rule

Get reclamation rule suggestions

Update existing reclamation rules with VIP condition

-   **Conversational topics**

Get products for reclamation rule creation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sam\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sam\_admin

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

Create software reclamation rule Agentic workflow

</td></tr></tbody>
</table>Learn more about Software Asset Management at [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SoftwareAssetMgmt.md).

**Parent Topic:**[Software Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sam-ai-agents-overview.md)

