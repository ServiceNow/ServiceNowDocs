---
title: Microsoft Intune group creation management AI agent
description: This AI agent creates Microsoft 365 or security groups in Microsoft Intune. It collects the group details, suggests a group description, confirms the request with the user, and reports the result or any error.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/inth-csdv2-microsoft-intune-group-creation-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Client Software Distribution 2.0 AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI assets, Enable AI experiences]
---

# Microsoft Intune group creation management AI agent

This AI agent creates Microsoft 365 or security groups in Microsoft Intune. It collects the group details, suggests a group description, confirms the request with the user, and reports the result or any error.

## Workflow

The agent helps the user create a Microsoft 365 or security group in Microsoft Intune.

1.  Ask the user whether to create a Microsoft 365 group or a security group.
2.  Ask for the group name and email alias.
3.  Suggest a group description and let the user accept it or provide their own.
4.  Summarize the group details and ask the user to confirm before creating it.
5.  Create the group and report its name and ID, or explain any error that occurred.

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

-   **Subflow**

Create Group


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

