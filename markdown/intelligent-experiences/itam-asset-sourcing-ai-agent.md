---
title: Asset sourcing AI agent
description: This AI agent helps source a requested item by generating and executing sourcing plans through consumption, transfer, and purchase. The agent creates plans autonomously or with user guidance, coordinates with external agents for transfer and purchase orders, and validates sourcing status throughout the process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itam-asset-sourcing-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Asset Management AI agents, IT Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Asset sourcing AI agent

This AI agent helps source a requested item by generating and executing sourcing plans through consumption, transfer, and purchase. The agent creates plans autonomously or with user guidance, coordinates with external agents for transfer and purchase orders, and validates sourcing status throughout the process.

## Workflow

The agent sources a requested item by executing three independent flows in sequence: auto source, guided source, and user input source.

1.  Verify that a requested item number is provided and retrieve the item details, including quantity and model name.
2.  Attempt to source the item automatically using the auto source plan flow, consuming, transferring, or purchasing assets as determined by the generated plan.
3.  If the item is not fully sourced, generate a guided source plan, present it to the user for confirmation, and execute the approved plan steps.
4.  If the item still requires sourcing, generate a user input source plan and prompt the user to confirm transfer and purchase actions as needed.
5.  Validate the sourcing status after each phase and notify the user when all requested quantity has been sourced or if quantity remains outstanding.

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

Auto consume the assets for the requested items

Consume the assets for the requested items

Fetch the details of the requested item

Generate auto source plan for the requested item

Generate guided source plan for the requested item

Generate user input plan for the requested item

Validate the source plan

Validate the sourcing status of requested item


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

procurement\_user

</td></tr><tr><td>

Data access roles

</td><td>

procurement\_user, sn\_request\_write

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

Help manage enterprise asset requests

</td></tr></tbody>
</table>Learn more about IT Asset Management at .

**Parent Topic:**[IT Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itam-ai-agents-overview.md)

