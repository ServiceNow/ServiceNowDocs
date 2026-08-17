---
title: Microsoft license assignment AI agent
description: This Software Asset Management agent assigns a Microsoft license to a user for a given request item, handling integration profile selection, reservation order creation, and Entra ID group assignment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sam-microsoft-license-assignment-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Software Asset Management AI agents, Software Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Microsoft license assignment AI agent

This Software Asset Management agent assigns a Microsoft license to a user for a given request item, handling integration profile selection, reservation order creation, and Entra ID group assignment.

## Workflow

1.  Run the Microsoft License Assignment tool with the request item number. If it returns an error, stop immediately.
2.  If integration profiles are available, prompt the user to select one and re-run the tool with the selection.
3.  If licenses aren't currently available but entitlement details exist, offer to create a reservation order. Show the draft order for review, allow date adjustments \(validated against the entitlement date range\), and create the order.
4.  Review existing Entra ID groups that carry the same license. If multiple groups are found, prompt the user to select one. If only one exists, use it automatically.
5.  Assign the license to the user, including the selected group if applicable.

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

AssignLicenseToUser

Microsoft License Assignment

ReviewExistingEntraIDGroups


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

procurement\_user

</td></tr><tr><td>

Data access roles

</td><td>

procurement\_user, itil, now\_assist\_panel\_user

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

Help manage software requests

</td></tr></tbody>
</table>Learn more about Software Asset Management at [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SoftwareAssetMgmt.md).

**Parent Topic:**[Software Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sam-ai-agents-overview.md)

