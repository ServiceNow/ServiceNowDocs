---
title: Move order voice AI voice agent
description: The AI voice agent helps a caller move their telecom service to a new address. It collects the caller's details over the phone, matches them to existing records, checks that the service is available at the new address, and creates a move order.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/tmt-move-order-voice-ai-voice-agent.html
release: brazil
topic_type: reference
last_updated: "2026-11-04"
reading_time_minutes: 2
breadcrumb: [Sales CRM for Telecommunications AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Move order voice AI voice agent

The AI voice agent helps a caller move their telecom service to a new address. It collects the caller's details over the phone, matches them to existing records, checks that the service is available at the new address, and creates a move order.

## Workflow

The agent helps the user move an existing telecom service, such as a broadband connection, to a new service address.

1.  Greet the user, confirm that they want to move their service to a new address, and note any details they've already mentioned.
2.  Verify that the user is a valid consumer.
3.  Find the user's active services at their current service location.
4.  Ask for the current service location if it's missing, and confirm that the location exists.
5.  Ask for the new service address if it's missing, and create a location record for it if one doesn't already exist.
6.  Check that the product offering can be serviced at the new address.
7.  Create the move order and give the user the order number.
8.  Ask whether the user needs anything else, and end the call when they're done.

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

Check Serviceability

Create Location For Consumer

Create Move Order

Fetch Consumer Location

Fetch Consumer Service

Validate Consumer


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_customerservice\_manager
-   sn\_ind\_tmt\_orm.order\_creator
-   snc\_internal

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Sales CRM for Telecommunications at [Sales Customer Relationship Management for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/sales-crm.md).

**Parent Topic:**[Sales CRM for Telecommunications AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/somt-ai-agents-overview.md)

