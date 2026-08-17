---
title: Asset next best action AI agent
description: This AI agent guides users through the repair order task process by validating task numbers, identifying task types, and routing the workflow to the correct specialized agent for troubleshooting or repair. The agent processes one task at a time to ensure accurate handling of hardware asset repair order tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itam-asset-next-best-action-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Asset Management AI agents, IT Asset Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Asset next best action AI agent

This AI agent guides users through the repair order task process by validating task numbers, identifying task types, and routing the workflow to the correct specialized agent for troubleshooting or repair. The agent processes one task at a time to ensure accurate handling of hardware asset repair order tasks.

## Workflow

The agent identifies a repair order task type and routes the work to the appropriate specialized agent for completion.

1.  Verify that a repair order task number is provided, prompting the user if it is missing.
2.  Retrieve the task details and perform validation to confirm the task name, asset information, and status.
3.  If validation returns an error, inform the user and end execution.
4.  Display the identified task details to the user, including the task name, asset model, and manufacturer.
5.  Route to the appropriate workflow: if the task name is Troubleshoot Asset, invoke the evaluate asset flow; if the task name is Repair Asset, invoke the repair asset flow.
6.  Terminate the workflow after the appropriate section has completed execution.

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

Get task details and perform validation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

inventory\_user

</td></tr><tr><td>

Data access roles

</td><td>

inventory\_user, 8c5ce94b77ac4210fa3fca22fe5a994b

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

-   Help repair enterprise assets
-   Help repair hardware assets

</td></tr></tbody>
</table>Learn more about IT Asset Management at .

**Parent Topic:**[IT Asset Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itam-ai-agents-overview.md)

