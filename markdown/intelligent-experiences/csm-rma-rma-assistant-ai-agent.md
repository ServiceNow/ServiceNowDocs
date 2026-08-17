---
title: RMA Assistant AI agent
description: This AI agent helps customers and human agents with RMA case creation and processing for product returns, repairs, and replacements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-rma-rma-assistant-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Customer Service Management AI agents, Customer Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# RMA Assistant AI agent

This AI agent helps customers and human agents with RMA case creation and processing for product returns, repairs, and replacements.

## Workflow

The agent helps users complete RMA tasks.

1.  Acknowledge concerns empathetically.
2.  Inform the user, "I understand this isn't fully addressing your needs."
3.  Wait for acknowledgment.
4.  Transfer to human agent.
5.  End chat only after confirmation.
6.  If user asks off-topic questions: Inform politely that this is not part of the RMA Case flow and offer to connect to live agent at the end.
7.  After live agent chat ends, or if no agents are found, close the flow smoothly with summary.

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

Check Product Exceptions

Check user has a Customer role

Create case line entitlements

Create RMA Case

Create RMA Case Line

Customer identification

Fetch Request Reason Code values

Fetch the associated case lines

Get the available entitlements

Get the Recommendations

Move case to Request info

Move case to WIP

Product Lookup

RMA Case lookup

Send summary email for RMA case

Update case lines

Update interaction record with account and contact

Update RMA case

Update RMA Case state

Valid RMA case number

-   **Topic Block**

Fetch User Context


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_csm\_rma\_case.csm\_rma\_case\_agent, sn\_customerservice.customer

</td></tr><tr><td>

Data access roles

</td><td>

Not defined.

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
</table>Learn more about Customer Service Management at [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md).

**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/csm-ai-agents-overview.md)

