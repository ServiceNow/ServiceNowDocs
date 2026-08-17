---
title: Change CI suggestion AI agent
description: This AI agent recommends a list of relevant configuration items \(CIs\) that can be added as Affected CIs to the current change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-change-ci-suggestion-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Change CI suggestion AI agent

This AI agent recommends a list of relevant configuration items \(CIs\) that can be added as Affected CIs to the current change request.

## Workflow

1.  Extract the current Change Request number and ask the user to confirm whether to proceed: `Do you need help in identifying configuration items for `{changeRequestNumber}`?`
2.  If the user confirms, proceed to the next step; otherwise end the conversation.
3.  Ask the user for details about the configuration items.
4.  Launch the Get configuration items tool for change based on user input tool and pass the user-provided utterance from the previous step as input.
5.  Present this tool's output to the user as a formatted list of CI suggestions.
6.  Based on the user's response, launch the associate configuration items to change tool and pass the selectedSysId variable as an input.
7.  Display the output to the user.

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

Associate configuration items to change

Get configuration items for change

Get configuration items for change based on user input

Get context


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

itil

</td></tr><tr><td>

Data access roles

</td><td>

itil, cmdb\_read

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

Suggest configuration items for a change request

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

