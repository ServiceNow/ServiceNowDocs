---
title: Shift and schedule management AI agent
description: This AI agent helps managers create, review, update, and delete shifts and schedules, and assign technicians to them. It suggests default shift details, finds technicians by skill or name, and asks the manager to confirm one complete plan before making changes. Managers can also open shifts for technician signup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/fsm-shift-and-schedule-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Field Service Management AI agents, Field Service Management, AI agents library, AI assets, Enable AI experiences]
---

# Shift and schedule management AI agent

This AI agent helps managers create, review, update, and delete shifts and schedules, and assign technicians to them. It suggests default shift details, finds technicians by skill or name, and asks the manager to confirm one complete plan before making changes. Managers can also open shifts for technician signup.

## Workflow

The agent helps managers create and manage shifts and schedules and assign technicians.

1.  Determine whether the manager wants to create, view, change, or delete shifts and schedules, or find technicians.
2.  Fill in any missing shift details using standard defaults, and search for technicians by skill or name.
3.  Display a summary of the plan and ask the manager to confirm, change, or cancel.
4.  After confirmation, create the shifts and schedule, then assign the technicians directly or open the shifts for signup.

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

Delete Schedule Plan

Display Shift/Schedule Summary Card

Display Signup Roster Card

Display Technician Selector Card

Get Users with Skills

Update Schedule Plan

executeSchedulePlan

getCommonlyUsedShift

getManagedAgents

manageSignup

readSchedulingData


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

wm\_manager

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

wm\_manager

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

-   Default VA Workflow
-   Shift and schedule management

</td></tr></tbody>
</table>**Parent Topic:**[Field Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/fsm-ai-agents-overview.md)

