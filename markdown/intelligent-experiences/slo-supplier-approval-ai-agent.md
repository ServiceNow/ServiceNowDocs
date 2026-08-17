---
title: Supplier approval AI agent
description: This Supplier Lifecycle Operations agent performs the supplier activation or supplier rejection tasks during supplier approval process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/slo-supplier-approval-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Supplier Lifecycle Operations AI agents, Supplier Lifecycle Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Supplier approval AI agent

This Supplier Lifecycle Operations agent performs the supplier activation or supplier rejection tasks during supplier approval process.

## Workflow

1.  Identify whether the request is for supplier activation or rejection.
2.  Confirm with the user that they want to proceed. If confirmed, execute the activation. If the user declines, switch to the rejection path.
3.  Ask the user for a rejection reason, then execute the rejection with that reason.

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

-   **Script**

Update supplier and supplier case status


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_supplier\_gen\_ai.now\_assist\_fulfiller, sn\_slm.owner

</td></tr><tr><td>

Data access roles

</td><td>

sn\_supplier\_gen\_ai.now\_assist\_fulfiller, sn\_slm.owner

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
</table>Learn more about Supplier Lifecycle Operations at [Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supp-mgmt-landing-page.md).

**Parent Topic:**[Supplier Lifecycle Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/slo-ai-agents-overview.md)

