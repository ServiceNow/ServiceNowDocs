---
title: Move order voice AI agent
description: This Sales Customer Relationship Management voice agent helps users relocate a telecom service to a new address by validating the consumer, verifying serviceability at the target location, and creating a move order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/som-move-order-voice-ai-voice-agent.html
release: australia
topic_type: reference
last_updated: "2026-07-24"
reading_time_minutes: 2
breadcrumb: [Sales Automation AI agents, Sales Automation, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Move order voice AI agent

This Sales Customer Relationship Management voice agent helps users relocate a telecom service to a new address by validating the consumer, verifying serviceability at the target location, and creating a move order.

## Workflow

1.  Confirm the user wants to move a telecom service to a new address, and extract any details already mentioned \(current location, product offering, new address\).
2.  Verify the current user is a valid consumer in the system.
3.  Fetch the consumer's services at their current location for the specified product offering.
4.  Confirm the existing service location is valid.
5.  Check if the target address already exists for the consumer. Create it if it doesn't exist.
6.  Verify the product offering is available at the new location.
7.  Build the product offering list from the consumer's active services and create the move order with the current location, new location, and consumer details.
8.  Inform the user of the move order number on success, or that creation failed, and ask if they need further help.

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

Check Serviceability

Create Location For Consumer

Create Move Order

Fetch Consumer Location

Fetch Consumer Service

Validate Consumer


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_customerservice.consumer

</td></tr><tr><td>

Data access roles

</td><td>

snc\_internal, sn\_customerservice\_manager, sn\_ind\_tmt\_orm.order\_creator

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Sales Customer Relationship Management at [Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-overview.md).

**Parent Topic:**[Sales Automation AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sales-automation-ai-agents-overview.md)

