---
title: Zero touch service desk agent
description: This AI agent investigates supplier invoice inquiry cases and generates a response for the supplier contact. Fulfillers can review its work in the Agentic Processes panel on the case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/zero-touch-service-desk-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Operations AI agents, Accounts Payable Operations \(APO\), AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Zero touch service desk agent

This AI agent investigates supplier invoice inquiry cases and generates a response for the supplier contact. Fulfillers can review its work in the Agentic Processes panel on the case.

## Workflow

The agent helps users complete tasks related to recommend invoice owner.

1.  Investigate the invoice inquiry case.
2.  Generate a response, which appears in the Review output section.
3.  Set the invoice inquiry case state to Awaiting acceptance.
4.  Notify the requester about the resolution through the Supplier Collaboration Portal.

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

-   **Script**

Get supplier contacts


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_ap\_fulfiller

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_ap\_fulfiller

</td></tr><tr><td>

Triggers

</td><td>

For APO, the APO Assignment Rule assigns AP cases \(`sn_ap_cm_ap_case`\) to the AI L1 APO Service Desk Specialist user and the Accounts Payable AI L1 Support group when all of the following are true: -   The sub-category is Invoice inquiry or Payment inquiry.
-   The state is New.
-   The assignment group is empty.

</td></tr><tr><td>

Channels

</td><td>

Activity stream, for both inbound and outbound messages.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

The agent runs through the L1 APO Service Desk Specialist \(APO - ZTSD Worker Template\).

</td></tr></tbody>
</table>For more information on Accounts Payable Operations, see [Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/acc-pay-mgmt-landing-page.md).

**Parent Topic:**[Accounts Payable Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/accounts-payable-operations-ai-agents-overview.md)

