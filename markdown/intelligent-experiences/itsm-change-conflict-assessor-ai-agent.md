---
title: Change conflict assessor AI agent
description: This AI agent can assess conflicts for changes. This includes checking mandatory fields and trigger conflict detection, and updating worknotes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-change-conflict-assessor-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Change conflict assessor AI agent

This AI agent can assess conflicts for changes. This includes checking mandatory fields and trigger conflict detection, and updating worknotes.

## Workflow

The agent shows users a summary of conflicts and impacted services and CIs.

1.  Use the Get Change request information tool to retrieve information for the change request.
2.  Check the change request for the configuration item field.
3.  Check the change request for the planned start date and planned end date fields.
4.  Show these values to the user.
5.  Verify whether a conflict check has run for the change request. If yes, ask the user if they want to run it again. If no, then run it without asking.
6.  Use the Get list of conflicts for the Change Request group by conflict type tool to find conflicts related to the change request.
7.  Show results to the user.
8.  Update worknotes if the user approves.

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

Check if conflict check has run for the Change

Display Change's configuration item and planned start date and planned end date

Display conflicts summary

Display impacted services/CIs summary

Get Change request information

Get list of conflicts for the Change Request group by conflict type

Get list of impacted services/CIs for the Change Request

Run conflict detection for the Change Request with timeout

Set Change Work Note

Update Change request's planned start date and planned end date


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_itsm\_aia.sn\_aia\_chg\_conflict

</td></tr><tr><td>

Data access roles

</td><td>

itil, sn\_change\_write

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

Assess conflicts for a change request

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

