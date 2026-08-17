---
title: Change request plans AI agent
description: This AI agent helps change owners and approvers by drafting high-quality, context-aware change request content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-change-request-plans-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Change request plans AI agent

This AI agent helps change owners and approvers by drafting high-quality, context-aware change request content.

## Workflow

The agent drafts implementation plans, backout plans, test plans, justifications, and risk &amp; impact analyses.

1.  Fetch the change request details.
2.  Generate all plans.
3.  Present each plan individually, asking the user if they want to proceed.
4.  Revise draft \(if feedback provided\).
5.  Update change request record when approved.
6.  Continue to the next plan until finished.

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

Generate Change request Plans

Get current change request details

Update plans to change request


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

itil

</td></tr><tr><td>

Data access roles

</td><td>

itil

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

Generate change request plans

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

