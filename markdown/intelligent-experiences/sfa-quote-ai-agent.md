---
title: Quote AI agent
description: This AI agent helps sales agents create, update, and finalize quotes. It validates products against the catalog, adds and configures line items, applies discounts, and generates the quote document. When started from an opportunity, it reads the opportunity line items and notes to build the quote without manual input.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/sfa-quote-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales CRM AI agents, Sales CRM, AI agents library, AI assets, Enable AI experiences]
---

# Quote AI agent

This AI agent helps sales agents create, update, and finalize quotes. It validates products against the catalog, adds and configures line items, applies discounts, and generates the quote document. When started from an opportunity, it reads the opportunity line items and notes to build the quote without manual input.

## Workflow

The agent helps sales agents build a complete quote from an opportunity or an account, from adding products through to the final quote document.

1.  Ask for an opportunity number or account name if neither was provided.
2.  Create the quote, and when it starts from an opportunity, bring in the opportunity line items and suggest more products based on the opportunity notes and comments.
3.  Look up each requested product in the product catalog, and ask you to choose when there are several matches.
4.  Configure configurable products using natural language requirements, and add other products to the quote as line items.
5.  Apply line or quote discounts that you request or that your description of the deal suggests, after confirming the discount details with you.
6.  Generate the quote document and share the link when no line item, configuration, or discount work is pending.
7.  Send an email notification summarizing the quote to the sales agent.

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

-   **Flow actions**

AI product search

Apply Quote Discount

Create New Quote

Create Quote Line Item

Generate Quote PDF

Get Opportunity details

Get Quote details

Lookup Product Deterministic

Lookup Quote Line

Notify Sales Rep via Email

Update Quote Fields

Update Quote Line

-   **Scripts**

trigger\_discount\_approval\_workflow

-   **Subflows**

Call Config AI


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_qut\_sum\_skill.quote\_ai

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_qut\_sum\_skill.quote\_ai

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

Quote agent workflow

</td></tr></tbody>
</table>Learn more about Quote Management at .

**Parent Topic:**[Sales Automation AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/sales-automation-ai-agents-overview.md)

