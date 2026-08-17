---
title: Hardware Asset Management sourcing AI agent
description: This AI agent helps to source a requested hardware item through consume, transfer, and purchase.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ham-hardware-asset-management-sourcing-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Hardware Asset Management AI agents, Hardware Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Hardware Asset Management sourcing AI agent

This AI agent helps to source a requested hardware item through consume, transfer, and purchase.

## Workflow

The agent helps users complete tasks related to hardware asset management sourcing.

1.  Prompt the user for an item number, if not already provided.
2.  Use the Fetch the details of the requested item tool to retrieve information for the requested item number.
3.  If there's no error, inform the user of the required quantity.
4.  Execute workflow A, which sources the item. If auto\_consume, auto\_transfer, and auto\_purchase are true, and there are no problems, validate the sourcing for the user. If successful, continue to the next step.
5.  Execute workflow B, which generates a guided source plan for the requested hardware. The user must approve this plan. If successful, continue to the next step.
6.  Execute workflow C, which generates the input plan for the requested hardware. The user must approve this plan.
7.  End workflow when C completes.

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

Auto consume the assets for the requested hardware items

Consume the assets for the requested hardware items

Fetch the details of the requested item

Generate auto source plan for the requested hardware item

Generate guided source plan for the requested hardware item

Generate user input plan for the requested hardware item

Validate the source plan

Validate the sourcing status of requested item


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

procurement\_user

</td></tr><tr><td>

Data access roles

</td><td>

procurement\_user, itil

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

Help manage hardware asset requests

</td></tr></tbody>
</table>Learn more about Hardware Asset Management at [Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/ham-landing-page.md).

**Parent Topic:**[Hardware Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ham-ai-agents-overview.md)

