---
title: Lead outreach AI agent
description: This AI agent sends outreach and follow-up emails to new leads on behalf of sales agents. It selects the email template based on how many emails the lead has already received, and disqualifies the lead when three emails go unanswered.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/sfa-lead-outreach-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI assets, Enable AI experiences]
---

# Lead outreach AI agent

This AI agent sends outreach and follow-up emails to new leads on behalf of sales agents. It selects the email template based on how many emails the lead has already received, and disqualifies the lead when three emails go unanswered.

## Workflow

The agent helps sales agents engage new leads by sending outreach and follow-up emails without asking for confirmation at each step.

1.  Fetch the lead details and the emails already sent to the lead.
2.  If the lead has received two or fewer emails, select the next email template in sequence, starting with the outreach email and followed by each follow-up email.
3.  Personalize the email with the lead's name and the lead owner's name, and include any previously sent emails in chronological order.
4.  Send the email to the lead.
5.  Create a follow-up event for the next email.
6.  Update the lead stage to Contacted if it isn't already set.
7.  If the lead has received more than two emails without responding, work with other AI agents to disqualify the lead.

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

-   **Record operations**

Fetch email templates

Fetch sent emails to lead

-   **Scripts**

Create follow up event for next email

Fetch lead details

Update the lead stage

-   **Subflows**

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

