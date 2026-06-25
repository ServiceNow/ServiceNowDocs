---
title: Schedule Management in CSM Configurable Workspace Workforce Optimization for Customer Service
description: Schedule Management schedule management is a standalone capability within Workforce Optimization for Customer Service that allows supervisors and managers to create, view, and manage team schedules independently of other WFO modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/schedule-management-capabilities-in-csm-configurable-workspace.html
release: australia
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 3
breadcrumb: [Optimize workforce operations, Extend capabilities, Configure, Customer Service Management]
---

# Schedule Management in CSM Configurable Workspace Workforce Optimization for Customer Service

Schedule Management schedule management is a standalone capability within Workforce Optimization for Customer Service that allows supervisors and managers to create, view, and manage team schedules independently of other WFO modules.

Roles: sn\_shift\_planning.admin, sn\_shift\_planning.manager.

Schedule management schedule management provides supervisors and managers with tools to manage agent schedules, shifts, time off requests, and schedule adherence from the CSM workspace. You can activate and use Schedule Management schedule management without enabling Forecasting, Intraday Management, Coaching, or other WFO modules.

The modular design supports organizations in CSM, FSM, and Retail, that require shift and roster management capabilities without the full WFO suite.

Schedule Management schedule management provides the following capabilities:

-   Create and manage agent schedules within assigned groups.
-   View team calendars with shifts, on-call rotations, time off, meetings, and trainings.
-   Review and approve shift swap requests between agents.
-   Manage time off requests and reflect approved leave in the team calendar.
-   Monitor schedule adherence and conformance using built-in visualizations.
-   Access scheduling functionality directly from the CSM Configurable Workspace or CSM Agent Workspace.

## Schedule management module

The Schedule Management workspace is accessible from the navigation menu in the CSM Configurable Workspace. Select **Schedule** to open the workspace. The Team Calendar tab opens by default.

The workspace contains the following tabs:

<table id="table_smz_mv4_hjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Team calendar

</td><td>

-   Default view.
-   Displays a unified calendar of agent schedules within your managed groups.
-   Shows shifts, on-call rotations, time off, meetings, trainings, holidays, and other events. Supports day, week, and month view toggles.

</td></tr><tr><td>

Shifts

</td><td>

-   Lists all defined time periods, including shifts, on-call rotations and holiday spans.
-   Displays name, start time, end time, and assignment group.

</td></tr><tr><td>

Shift swap requests

</td><td>

-   Lists pending and processed shift exchange requests between agents.
-   Displays the requesting agent, receiving agent, original shift, and requested shift.
-   Supervisors and managers can approve or reject requests.

</td></tr><tr><td>

Time off requests

</td><td>

-   Displays leave requests that affect scheduling coverage. Shows agent name, assignment group, time range, and request status.
-   Approved requests appear as events in the Team Calendar.

</td></tr><tr><td>

Schedule adherence

</td><td>

Provides visualizations of agent adherence and conformance data to help identify coverage gaps and schedule deviations.

</td></tr></tbody>
</table>## Team Calendar toolbar

Use the toolbar on the right side of the **Team Calendar** screen to filter and navigate calendar data. You can filter by **Assignment Group**, **Agent**, or **Event Type**. Filters update the calendar view dynamically. Use the date navigation controls to switch between weeks and days. Select **Reset** to return the calendar to the default view.

## Roles and access

Schedule Management schedule management uses a role hierarchy based on the platform-standard Agent Group Management model. Manager visibility and permissions are determined by agent-to-group relationships, not WFO-specific configurations. This aligns scheduling access with the standard platform identity model and supports consistent access management across CSM, FSM, and Retail.

The following roles are available:

|Role|Persona|Capabilities|
|----|-------|------------|
|sn\_shift\_planning.admin|Manager|Full access to scheduling configuration, event categories, and location schedules.|
|sn\_shift\_planning.manager|Agent|Approve or reject shift schedules and registrations, manage shifts and shift agents, manage agent availability and time attendance.|
|sn\_shift\_planning.agent|User|View own schedule and submit shift swap and time-off requests.|
|sn\_shift\_planning.user|User|Base read access only.|

**Note:** If you have the sn\_csm\_wfo\_workspa.admin or sn\_csm\_wfo\_workspa.manager role, you can automatically inherit the corresponding sn\_shift\_planning role.

-   **[Schedule Management standalone activation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/schedule-management-as-a-standalone-activation.md)**  
Schedule Management as a standalone plugin supports to manage agent schedules, team calendars, shift swaps, time off, and adherence, with access from supported CSM workspaces without requiring the full WFO suite.

**Parent Topic:**[Optimize workforce operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setup-configurable-wfo-cs.md)

**Related topics**  


[Channel Management in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/explore-channels-configurable-wfo-cs.md)

[Using Channel Management in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configurable-channels-wfo-cs.md)

[Decouple Channel Management dependencies from WFO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/decouple-channel-management-dependencies-from-wfo.md)

