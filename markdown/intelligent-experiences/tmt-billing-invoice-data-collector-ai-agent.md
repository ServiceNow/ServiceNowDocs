---
title: Billing invoice data collector AI agent
description: This Telecommunications, Media, and Technology \(TMT\) agent provides detailed information about invoices, validates amounts, and identifies high-amount line items for billing inquiries. The agent retrieves invoice history, communicates invoice and line item details to the user, and flags potential causes of high charges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/tmt-billing-invoice-data-collector-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Billing invoice data collector AI agent

This Telecommunications, Media, and Technology \(TMT\) agent provides detailed information about invoices, validates amounts, and identifies high-amount line items for billing inquiries. The agent retrieves invoice history, communicates invoice and line item details to the user, and flags potential causes of high charges.

## Workflow

1.  Fetch the invoice history using the billing account number and extract the latest and previous invoices.
2.  Show the user the key details for each invoice: number, amount, usage billed through, and credited amount.
3.  If the latest invoice has a pending amount greater than zero, notify the user of the outstanding balance and due date.
4.  Fetch detailed line items for the latest invoice and present them to the user. If the line items can't be retrieved, inform the user and stop.
5.  If the latest invoice amount is higher than the previous invoice, identify the line item responsible for the increase. Inform the user which item likely caused the higher bill. If the latest invoice is not higher, return control to the orchestrator.

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

Get high amount line item

Get Invoice Details

Get Invoice History


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_tmt\_agentic\_ai.telco\_billing\_inquiry\_case\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_tmt\_agentic\_ai.telco\_billing\_inquiry\_case\_agent

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Not defined.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Help remediate bill issues

</td></tr></tbody>
</table>Learn more about Supplier Lifecycle Operations at [Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supp-mgmt-landing-page.md).

**Parent Topic:**[Telecommunications, Media and Technology AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/tmt-ai-agents-overview.md)

