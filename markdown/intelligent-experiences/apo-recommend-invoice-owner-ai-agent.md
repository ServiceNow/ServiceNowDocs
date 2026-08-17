---
title: Recommend invoice owner AI agent
description: This AI agent intelligently analyzes exception work notes to predict the most likely business owner for an invoice. It collaborates with the Accounts Payable \(AP\) specialist — the person responsible for processing the invoice — by suggesting the predicted business owner or creating follow-up tasks to streamline ownership validation and resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/apo-recommend-invoice-owner-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Operations AI agents, Accounts Payable Operations \(APO\), Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Recommend invoice owner AI agent

This AI agent intelligently analyzes exception work notes to predict the most likely business owner for an invoice. It collaborates with the Accounts Payable \(AP\) specialist — the person responsible for processing the invoice — by suggesting the predicted business owner or creating follow-up tasks to streamline ownership validation and resolution.

## Workflow

The agent helps users complete tasks related to recommend invoice owner.

1.  Execute the "Retrieve recommendation from Exception Record" tool.
2.  If there are no invoices present, ask the AP specialist if they want to reach out to a supplier contact with an exception task.
3.  If the recommendation mentions that there are processed invoices present, but the match score is less than the threshold value, inform the AP specialist that a recommendation cannot be made, but the agent can suggest the business owner from the last processed invoice.
4.  If the recommendation mentions that the business owner was identified but auto-approval is disabled, then ask the AP specialist whether the mentioned business owner can be assigned to the invoice.

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

Create exception task

Get BO of last processed invoice

Get supplier contacts

Retrieve recommendation from Exception Record

Update BO on invoice


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ap\_apm.accounts\_payable\_specialist

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ap\_apm.accounts\_payable\_specialist

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>For more information on Accounts Payable Operations, see [Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/acc-pay-mgmt-landing-page.md).

**Parent Topic:**[Accounts Payable Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/accounts-payable-operations-ai-agents-overview.md)

