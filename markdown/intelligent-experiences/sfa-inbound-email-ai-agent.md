---
title: Inbound email AI agent
description: This AI agent analyzes the latest email that a lead sends in response to outreach and helps sales agents decide how to move forward. It classifies the response and then books a demo, disqualifies the lead, cancels the appointment, or drafts answers to the lead's questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/sfa-inbound-email-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI assets, Enable AI experiences]
---

# Inbound email AI agent

This AI agent analyzes the latest email that a lead sends in response to outreach and helps sales agents decide how to move forward. It classifies the response and then books a demo, disqualifies the lead, cancels the appointment, or drafts answers to the lead's questions.

## Workflow

The agent helps sales agents respond to leads by analyzing the lead's latest email and taking the matching action without asking for confirmation at each step.

1.  Fetch the lead details and update the lead stage to Nurturing if it isn't already set.
2.  Fetch the latest email from the lead, and notify the user and stop if no email is found.
3.  Classify the response as interest in booking or rescheduling a demo, not interested, cancellation of a scheduled demo, or additional questions when the intent is unclear.
4.  If the lead wants to book or reschedule a demo, work with other AI agents to start the appointment booking.
5.  If the lead isn't interested, work with other AI agents to disqualify the lead.
6.  If the lead wants to cancel a scheduled demo without rescheduling, cancel the appointment.
7.  If the lead has additional questions, prepare a response and show the questions and the response to the user.

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

Fetch latest email

Fetch lead details

Update the lead stage


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

[Help nurture new leads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/help-nurture-new-leads-agentic-workflow.md)

</td></tr></tbody>
</table>Learn more about Lead Management at [Lead Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/lead-management.md).

**Parent Topic:**[Sales Automation AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/sales-automation-ai-agents-overview.md)

