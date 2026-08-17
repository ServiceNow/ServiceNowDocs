---
title: Software removal candidate evaluation AI agent
description: This Software Asset Management agent identifies unused or underused software licenses and initiates reclamation after user confirmation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sam-software-removal-candidate-evaluation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Software Asset Management AI agents, Software Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Software removal candidate evaluation AI agent

This Software Asset Management agent identifies unused or underused software licenses and initiates reclamation after user confirmation.

## Workflow

1.  Identify the target product. If a Product ID is provided, use it directly. Otherwise, present available products for the user to select, optionally filtered by Publisher ID.
2.  Fetch removal candidate analysis data for the selected product. If no data is found, inform the user and end.
3.  Validate that the data supports reclamation. The checks differ based on software type \(installed vs. subscription\) but follow the same pattern: confirm recent usage or activity data exists, and confirm the ratio of removal candidates to total installations or subscriptions is within an acceptable range. If any check fails, inform the user with a specific reason and end.
4.  Present the number of eligible removal candidates and ask the user to confirm reclamation. Only non-VIP users with notifications enabled are included.
5.  Run the reclamation workflow and report the result. If successful and there are candidates stuck in "Awaiting Revocation" status for 60 days, flag them for review.

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

Find activity job status of the product

Find removal candidates analysis

Reclaim removal candidates

-   **Conversational topic**

Get products for removal candidate


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sam\_user

</td></tr><tr><td>

Data access roles

</td><td>

sam\_user

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

Evaluate software removal candidate Agentic workflow

</td></tr></tbody>
</table>Learn more about Software Asset Management at [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SoftwareAssetMgmt.md).

**Parent Topic:**[Software Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sam-ai-agents-overview.md)

