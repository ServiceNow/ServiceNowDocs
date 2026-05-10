---
title: Scheduling components in Workforce Optimization for ITSM
description: Workforce Optimization for ITSM has roles to administer agent shifts and schedules and properties to configure default behavior.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Scheduling components in Workforce Optimization for ITSM

Workforce Optimization for ITSM has roles to administer agent shifts and schedules and properties to configure default behavior.

## Roles

<table id="table_ztx_jwc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Shift Planning User \[sn\_shift\_planning.user\]

</td><td>

Grants read access for scheduling including the ability to view schedules and shifts.

</td><td>

 

</td></tr><tr><td>

Shift Planning Agent \[sn\_shift\_planning.agent\]

</td><td>

Grants agents access to their calendar. Agents can request shift swap or time off.

</td><td>

sn\_shift\_planning.user

</td></tr><tr><td>

Shift Planning Admin \[sn\_shift\_planning.admin\]

</td><td>

Grants administrative access to create, read, update, and delete \(CRUD\) schedules and work shifts.

</td><td>

-   sn\_shift\_planning.approver
-   sn\_shift\_planning.user
-   sn\_shift\_planning.agent

</td></tr></tbody>
</table>## Properties

<table id="table_ywt_4t1_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_itsm\_ mobile\_agent.events\_query\_days\_past

</td><td>

The maximum number of days past events for your shifts can be displayed on your mobile application. You can enter values that range from -1 to -31. -   **Type:** Integer
-   **Default value:** -31

</td></tr><tr><td>

sn\_itsm\_ mobile\_agent.events\_query\_days\_future

</td><td>

The maximum number of days future events for your shifts can be displayed on your mobile application. You can enter values that range from 1 to 90.-   **Type:** Integer
-   **Default value:** 90

</td></tr><tr><td>

sn\_uib\_agent\_sp.allow\_agent\_edit\_break

</td><td>

Enables agents to edit the start and end time of their break time in a shift span.-   **Type:** true\|false
-   **Default value:** false

</td></tr><tr><td>

sn\_uib\_agent\_sp.allow\_agent\_add\_remove\_break

</td><td>

Enables agents to add or remove their break time in a shift span.-   **Type:** true\|false
-   **Default value:** false

</td></tr><tr><td>

sn\_shift\_planning.number\_of\_days\_to\_cache

</td><td>

Number of days to cache agent schedules.-   **Type:** Integer
-   **Default value:** 5

</td></tr><tr><td>

sn\_shift\_planning.max\_shifts\_to\_autoassign

</td><td>

Number of preferred shifts from a schedule plan that will be auto-assigned. -   **Type:** Integer
-   **Default value:** 1

</td></tr><tr><td>

sn\_shift\_planning.max\_shifts\_allowed\_for\_signup

</td><td>

The maximum number of shifts that agents can sign up for within a schedule plan. -   **Type:** Integer
-   **Default value:**1

</td></tr><tr><td>

sn\_shift\_planning.enable\_agent\_signup

</td><td>

Enable agents to sign up for their own shifts. -   **Type:** true\|false
-   **Default value:**true

</td></tr><tr><td>

sn\_shift\_planning.enable\_schedule\_signup\_link

</td><td>

Enables or disables the link in the Upcoming section in the Service Operations Workspace landing page where agents can view shifts that they've signed up for that are due on the current day and the day after the current day. -   **Type:**true\|false
-   **Default value:** true

</td></tr><tr><td>

sn\_shift\_planning.days\_to\_signup\_due\_date

</td><td>

The number of days before the shift sign-up due date when agents and managers are notified. -   **Type:** Integer
-   **Default value:** 2

</td></tr><tr><td>

sn\_shift\_planning.display\_shift\_name

</td><td>

Set this property to true to display the shift name. If the value is set to false, the event type will be displayed.-   **Type:** Boolean
-   **Default value:** True

**Note:** It will take 24 hours for any changes you make to the property value to take effect. To view the changes immediately, run the **Shift Planning - Delete All Agent Schedules Cache** scheduled job.

</td></tr><tr><td>

assignShiftAgentsTypeaheadDisableAutoClose

</td><td>

Turns off the closing of the **Assign agents to this shift** typeahead list every time an agent is selected.

In the application navigator, enter `sys_ux_page_property.LIST`and press **Enter**. -   **Type:**true\|false
-   **Default value:** false

</td></tr><tr><td>

sn\_wfo\_outlook.enable\_outlook\_sync

</td><td>

Set this property to **true** to turn on the synchronization between the agent's calendar and the Microsoft Outlook calendar.

-   **Type:** Boolean
-   **Default value:** False

</td></tr></tbody>
</table>## Scheduled jobs

<table id="table_vxk_ndy_pnb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shift Planning - Delete All Agent Schedules Cache

</td><td>

Deletes cache from the sn\_shift\_planning\_agent\_availability table.-   Runs automatically everyday at 2:30 am
-   Run this job on-demand when you import data.

</td></tr></tbody>
</table>## User preferences

Navigate to **All** &gt; **User Administration** &gt; **User Preferences** and add the preferences listed in the table below.

**Note:** To set a system-wide user preference, select the **System** check box.

For information on setting user preferences, see [User preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UserPreferences.md).

<table id="table_urf_2s3_dtb"><thead><tr><th>

User Preference

</th><th>

Description

</th></tr></thead><tbody><tr><td>

workspace.onCallShiftsPageSize

</td><td>

Set the maximum number of on-call shifts to view per page in the **On-call shifts** tab in the Shifts side panel.-   **Name:** workspace.onCallShiftsPageSize
-   **Type:** Integer
-   **Value:** Enter the preferred number of on-call shifts you want to view per page.

</td></tr><tr><td>

workspace.workShiftsPageSize

</td><td>

Set the maximum number of work shifts to view per page in the **Work shifts** tab in the Shifts side panel.-   **Name:** workspace.workShiftsPageSize
-   **Type:** Integer
-   **Value:** Enter the preferred number of work shifts you want to view per page.

</td></tr><tr><td>

workspace.schedulePlanPageSize

</td><td>

Set the maximum number of scheduling plans to view per page in the Schedules side panel.-   **Name:** workspace.schedulePlanPageSize
-   **Type:** Integer
-   **Value:** Enter the preferred number of schedules you want to view per page.

</td></tr></tbody>
</table>