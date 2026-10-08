---
title: Microsoft Intune group deletion management AI agent
description: This AI agent deletes groups in Microsoft Intune. It confirms the deletion with the user and, when applications are assigned to the group, lets the user delete those assignments, keep them, or cancel the deletion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/inth-csdv2-microsoft-intune-group-deletion-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Client Software Distribution 2.0 AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI assets, Enable AI experiences]
---

# Microsoft Intune group deletion management AI agent

This AI agent deletes groups in Microsoft Intune. It confirms the deletion with the user and, when applications are assigned to the group, lets the user delete those assignments, keep them, or cancel the deletion.

## Workflow

The agent helps the user delete a group in Microsoft Intune.

1.  Ask the user for the group name or ID.
2.  Look up the group by name and, if several match, ask the user to choose the correct one.
3.  Ask the user to confirm the deletion.
4.  Check whether any application assignments use the group and, if so, list them.
5.  Ask whether to delete those application assignments first, delete the group without removing them, or cancel the deletion.
6.  Delete the group and report the result, or explain any error that occurred.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Look up Application Dependencies by Group ID

Look up Group by Name

-   **Subflow**

Delete Application Assignment

Delete Group


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_csd.CSD Admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_csd.CSD Admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Microsoft Intune Group Management Agentic Team

</td></tr></tbody>
</table>**Parent Topic:**[Client Software Distribution 2.0 AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/inth-csdv2-ai-agents-overview.md)

**Related topics**  


[Client Software Distribution 2.0 application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/csd-app-2.md)

[Integration Hub solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/solutions.md)

