---
title: AICT life cycle task reminder AI agent
description: This AI agent sends automated email reminders to task owners for overdue and dormant life cycle tasks on high-priority AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/plat-ai-aict-lifecycle-task-reminder-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI assets, Enable AI experiences]
---

# AICT life cycle task reminder AI agent

This AI agent sends automated email reminders to task owners for overdue and dormant life cycle tasks on high-priority AI assets.

## Workflow

This agent runs automatically on a schedule or triggered event, identifies overdue assessment tasks across high-priority AI assets, and sends targeted email reminders to assigned task owners.

1.  Collect all life cycle tasks from high-priority assets using the Query life cycle Tasks tool.
2.  Filter tasks to identify overdue and dormant items based on due date and last activity.
3.  For each overdue task, retrieve the task owner contact information and asset context.
4.  Compose and send personalized email reminders including task details, asset name, and deadline.
5.  Log all reminders sent and report delivery status.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Query life cycle Tasks for Asset

Report Agent Action Status

Send life cycle Task Reminder Emails


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/platform-ai-agents-overview.md)

