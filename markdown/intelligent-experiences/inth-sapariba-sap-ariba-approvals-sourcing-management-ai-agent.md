---
title: SAP Ariba approvals sourcing management AI agent
description: This AI agent creates approval statuses in SAP Ariba to move sourcing approval workflows forward.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/inth-sapariba-sap-ariba-approvals-sourcing-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [SAP Ariba Spoke AI agents, Integration Hub AI agents, Integration Hub, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# SAP Ariba approvals sourcing management AI agent

This AI agent creates approval statuses in SAP Ariba to move sourcing approval workflows forward.

## Workflow

The agent helps the user record an approval status for a sourcing approval in SAP Ariba.

1.  Ask the user what they want to do and collect the details the action needs, such as the approval request and the status to set.
2.  Create the approval status for the specified approval request.
3.  Report the outcome to the user, including details of any error.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Action**

Create Approval Status


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Not defined.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Approval Status Lookup and Creation

</td></tr></tbody>
</table>**Parent Topic:**[SAP Ariba Spoke AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inth-sapariba-ai-agents-overview.md)

**Related topics**  


[SAP Ariba Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/sap-ariba-spoke.md)

[Integration Hub spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/spokes-list.md)

