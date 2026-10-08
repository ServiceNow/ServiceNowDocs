---
title: Lead disinterest AI agent
description: This AI agent handles lead disqualification and opt-out requests for sales agents. After the sales agent confirms, it cancels the lead's upcoming appointments, closes the related tasks, and disqualifies the lead.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sfa-lead-disinterest-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Lead disinterest AI agent

This AI agent handles lead disqualification and opt-out requests for sales agents. After the sales agent confirms, it cancels the lead's upcoming appointments, closes the related tasks, and disqualifies the lead.

## Workflow

The agent helps sales agents disqualify leads that aren't interested or have opted out.

1.  Share the lead details, a summary of the emails sent to the lead, and the reason for disqualification, if available.
2.  Ask the user to confirm whether to disqualify the lead.
3.  If the user confirms, cancel all upcoming appointments with the lead.
4.  Close all tasks related to the lead.
5.  Update the lead stage to Disqualified.

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

-   **Scripts**

Cancel all tasks

Update the lead stage

-   **Subflows**

Cancel all upcoming appointments


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_sales\_common.sales\_agent

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

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

[Help nurture new leads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/help-nurture-new-leads-agentic-workflow.md)

</td></tr></tbody>
</table>Learn more about Lead Management at [Lead Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/lead-management.md).

**Parent Topic:**[Sales Automation AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sales-automation-ai-agents-overview.md)

