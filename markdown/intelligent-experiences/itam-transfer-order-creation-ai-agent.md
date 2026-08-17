---
title: Transfer order creation AI agent
description: This AI agent is used for creating a transfer order to source a requested item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itam-transfer-order-creation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Asset Management AI agents, IT Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Transfer order creation AI agent

This AI agent is used for creating a transfer order to source a requested item.

## Workflow

The agent helps users complete tasks related to transfer order creation.

1.  Use the Get Destination Stockrooms for requested item tool to retrieve a list of destination stockrooms.
2.  Ask the user to select a stockroom if multiple choices are available. If none are available, end the workflow.
3.  Use the Get Source Stockrooms tool to retrieve a list of source stockrooms.
4.  Ask the user to select a source stockroom if multiple choices are available. If none are available, end the workflow.
5.  Use the Create transfer order using input source plan tool to create the Transfer Order Line with the user's selected source and destination stockroom details.
6.  Create the transfer order using the Create transfer order with guided source plan tool.
7.  Display results to the user.

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

Create transfer order for auto-source

Create transfer order using input source plan

Create transfer order with guided source plan

Get Destination Stockrooms

Get Source Stockrooms


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

procurement\_user

</td></tr><tr><td>

Data access roles

</td><td>

procurement\_user, itil, sn\_request\_write

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

-   Help manage hardware asset requests
-   Help manage enterprise asset requests

</td></tr></tbody>
</table>Learn more about IT Asset Management at .

**Parent Topic:**[IT Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itam-ai-agents-overview.md)

