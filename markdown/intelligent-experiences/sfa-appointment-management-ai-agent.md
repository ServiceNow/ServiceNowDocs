---
title: Appointment management AI agent
description: This AI agent manages appointments with leads on behalf of sales agents. It reads lead emails, checks the lead owner's availability, and either books an appointment or proposes two open time slots. It also cancels appointments when a lead asks and sends a confirmation email.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sfa-appointment-management-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Appointment management AI agent

This AI agent manages appointments with leads on behalf of sales agents. It reads lead emails, checks the lead owner's availability, and either books an appointment or proposes two open time slots. It also cancels appointments when a lead asks and sends a confirmation email.

## Workflow

The agent helps sales agents schedule or cancel appointments with leads based on the lead's email, without asking for confirmation at each step.

1.  Read the lead's email to determine whether the lead wants to book or cancel an appointment, and identify any preferred date, time, or time zone.
2.  Fetch the lead owner's available time for the requested period, and stop with a message to the user if no time is available.
3.  If the lead requests a specific time and the lead owner is free for a 30-minute meeting, create a lead task and an appointment for that time.
4.  Send the lead a confirmation email on behalf of the lead owner with the appointment time and time zone, and a note that a meeting invite follows.
5.  If the requested time isn't available or the lead gives no specific time, send the lead an email on behalf of the lead owner that offers two available 30-minute slots.
6.  If the lead asks to cancel, cancel the upcoming appointment and send the lead a confirmation email, or ask for clarification if no upcoming appointment exists.
7.  After canceling an appointment, work with other AI agents to disqualify the lead.

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

Get Lead Owner's Meeting Availability

Validate if lead owner is available

-   **Subflows**

Cancel appointment

Create lead task and appointment

Send an email to lead


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

