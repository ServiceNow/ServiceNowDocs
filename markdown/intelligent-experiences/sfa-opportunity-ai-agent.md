---
title: Opportunity AI agent
description: This AI agent helps the user read, create, update, and summarize opportunities and their related records, such as accounts, contacts, touchpoints, opportunity tasks, line items, and meetings. It previews changes to opportunities, accounts, contacts, and line items and makes them only after the user approves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sfa-opportunity-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Opportunity AI agent

This AI agent helps the user read, create, update, and summarize opportunities and their related records, such as accounts, contacts, touchpoints, opportunity tasks, line items, and meetings. It previews changes to opportunities, accounts, contacts, and line items and makes them only after the user approves.

## Workflow

The agent helps users manage opportunities and their related records through natural-language requests.

1.  Identify the action the user wants to take and the record it applies to, and ask a clarifying question if the request is unclear or not supported.
2.  Use the record the user names, or the record open in the workspace if the user doesn't name one.
3.  Retrieve and present the matching records or an opportunity summary, showing the first 10 results when more exist.
4.  When creating an opportunity, help the user choose a sales cycle type and a stage that belongs to it.
5.  Preview changes to opportunities, accounts, contacts, and line items, and apply them only after the user approves.
6.  Apply changes to touchpoints, opportunity tasks, competitors, associated contacts, and meetings directly.
7.  Report the result, including the reason for any failure, and provide up to three next steps the user can take.

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

Opportunity Create

Opportunity Lookup

Opportunity Update


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_sales\_common.sales\_agent
-   sn\_sales\_common.sales\_restricted\_agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_sales\_common.sales\_agent
-   sn\_sales\_common.sales\_restricted\_agent

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

Opportunity Agentic Workflow

</td></tr></tbody>
</table>Learn more about Opportunity Management at [Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/opportunity-management.md).

To manage opportunity records, see [Manage opportunity records using an AI interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/manage-opportunity-records.md).

**Parent Topic:**[Sales Automation AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sales-automation-ai-agents-overview.md)

