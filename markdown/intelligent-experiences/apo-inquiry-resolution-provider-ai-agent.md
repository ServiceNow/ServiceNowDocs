---
title: Inquiry resolution provider AI agent
description: This AI agent assists with invoice inquiries by providing resolution details based on the invoice and its related data. It is intended for use by Accounts Payable Operations agents handling invoice inquiries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/apo-inquiry-resolution-provider-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Accounts Payable Operations AI agents, Accounts Payable Operations \(APO\), Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Inquiry resolution provider AI agent

This AI agent assists with invoice inquiries by providing resolution details based on the invoice and its related data. It is intended for use by Accounts Payable Operations agents handling invoice inquiries.

## Workflow

The agent helps users complete tasks related to inquiry resolution provider.

1.  Use the "Invoice Inquiry resolution generator and case update" tool to extract invoice details, payment details, invoice lines, and tax lines for the provided invoice inquiry number.
2.  Once the plan is displayed to the user, ask the user if they want to close the case.
3.  Based on the user's response, either close the case or update the work notes.

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

Close the case

Invoice Inquiry resolution generator and case update


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ap\_cm.agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ap\_cm.agent

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

Not applicable.

</td></tr></tbody>
</table>For more information on Accounts Payable Operations, see [Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/acc-pay-mgmt-landing-page.md).

**Parent Topic:**[Accounts Payable Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/accounts-payable-operations-ai-agents-overview.md)

