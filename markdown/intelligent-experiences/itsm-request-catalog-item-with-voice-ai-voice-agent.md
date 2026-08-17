---
title: Request catalog item AI voice agent
description: This AI voice agent assists users in finding and delivering catalog items. If the item is not categorized as software, then the catalog link is sent through email or SMS. If the item is software, this agent will help create the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-request-catalog-item-with-voice-ai-voice-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Request catalog item AI voice agent

This AI voice agent assists users in finding and delivering catalog items. If the item is not categorized as software, then the catalog link is sent through email or SMS. If the item is software, this agent will help create the request.

## Workflow

The agent operates only within approved channels \(email, SMS\) and never creates, modifies, or deletes catalog items.

1.  Verify that you have a description of the catalog item the user wants. If not provided, ask them to describe it.
2.  Search for matching items.
3.  If there are multiple matches, ask clarifying questions.
4.  Check the catalog item "category" sys\_id and determine if the item is in the software category.
5.  Confirm any changes and place the order \(software\), or provide the user with the catalog item link.

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

-   **Flow Actions**

Gather catalog item variables

Assist with catalog request form

Modify catalog item

Create catalog item order

-   **Search retrieval**

Get relevant Catalog Items

-   **Subflows**

Send catalog link to email

Send catalog link to SMS


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

nobody

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
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

