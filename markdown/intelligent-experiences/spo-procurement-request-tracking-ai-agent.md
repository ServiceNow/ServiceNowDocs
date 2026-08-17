---
title: Procurement request tracking AI agent
description: This Sourcing and Procurement Operations agent provides a summary of a procurement request. It can provide current status and next steps for the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spo-procurement-request-tracking-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Sourcing and Procurement Operations AI agents, Sourcing and Procurement Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Procurement request tracking AI agent

This Sourcing and Procurement Operations agent provides a summary of a procurement request. It can provide current status and next steps for the request.

## Workflow

1.  Parse the user's message to determine what they're looking for and whether they've provided a specific record number.
2.  If no record number is provided, construct a query based on the user's intent and search for matching records. If nothing is found, rephrase the query and retry once before asking the user for more details.
3.  Present the search results and ask the user to select one.
4.  Run the summary tool against the selected record and the original question, display the result.

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

Get records data

Record summary


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_spend\_gen\_ai.now\_assist\_requester

</td></tr><tr><td>

Data access roles

</td><td>

sn\_shop.shopper, sn\_spend\_gen\_ai.now\_assist\_requester

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

Help fulfill procurement requests

</td></tr></tbody>
</table>Learn more about Sourcing and Procurement Operations at [Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/psm-overview.md).

**Parent Topic:**[Sourcing and Procurement Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/spo-ai-agents-overview.md)

