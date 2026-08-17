---
title: Billing account information collector AI agent
description: This Telecommunications, Media, and Technology \(TMT\) agent retrieves billing case and account details and communicates them to the user in a structured format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/tmt-billing-account-information-collector-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Billing account information collector AI agent

This Telecommunications, Media, and Technology \(TMT\) agent retrieves billing case and account details and communicates them to the user in a structured format.

## Workflow

1.  Fetch the billing inquiry case information using the case number already provided by the user.
2.  Pull the case account number and account name from the case details, then present them to the user.
3.  Fetch the billing account details using the case account information. If the billing account can't be found, ask the user to correct the case account number and retry.
4.  Show the billing account details to the user.

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

Fetch Billing Account Details

-   **Flow Action**

Fetch Current Billing Inquiry Case Details


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

