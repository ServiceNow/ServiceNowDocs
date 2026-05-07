---
title: Activity timer log
description: The activity timer log feature automatically tracks the time that agents spend working on cases and interactions in CSM Configurable Workspace. Agents can view a time log report to see detailed records of the time spent on projects and tasks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-22"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Activity timer log

The activity timer log feature automatically tracks the time that agents spend working on cases and interactions in CSM Configurable Workspace. Agents can view a time log report to see detailed records of the time spent on projects and tasks.

## Activity timer log overview

The activity timer log feature monitors agent activity and automatically tracks the time that agents spend working on case and interaction records. When the feature is activated, agents can see the **timer component** in the record header. This component displays how much time has passed on the current record. The timer component can detect when an agent is actively working on a record and when they move away from the tab. The timer automatically pauses when the agent navigates away from the tab and resumes when the agent returns to the tab.

Start and stop entries in the Time Entry table mark when an agent is actively working on a case or interaction.

-   A start entry is created when an agent:
    -   Creates a case or interaction
    -   Opens a case or interaction
    -   Returns to a tab in the workspace and continues working on a record.

        **Note:** This requires a manual page refresh. When an agent returns to a tab, the system displays the following message: "Time tracker is paused due to inactivity. Refresh the page to resume the timer."

-   A stop entry is created when an agent:
    -   Leaves a tab in the workspace and selects another tab
    -   Closes a case
    -   Assigns a case or interaction to another user
    -   Is inactive on the current tab for two minutes
    -   Logs out

The Time Entry table stores the start and stop events and the time captured for each start/stop pair. The system runs a scheduled job every 24 hours that aggregates this information and stores it in the Time Entry Aggregated table. Agents can view this aggregated time data in the [My Timelog list](csm-config-ws-time-tracking.md#time_tracker_my_timelog_list).

## Timer component

When the activity timer log feature has been configured, the timer component is displayed in the record header next to the short description. Agents can use this timer to view the time elapsed on a record.

![](../image/activity-timer-log-component.png "Case page with timer component")

## My Timelog list

For customer service agents and consumer agents, the List view in CSM Configurable Workspace includes the **Timelog** &gt; **My Timelog** list.

-   Selecting **My Timelog** displays a list of records that the agent has worked on. The entry for each record includes the start time and end time and the total time worked for that start/end pair. There can be multiple entries for a record.
-   Selecting a record in the **Record** column displays the timelog for that record, including the following fields:
    -   Agent Name
    -   Last Status
    -   Status Updated Time
    -   Start Time
    -   End Time
    -   Total Time Spent

The **My Timelog** list includes the following default filter conditions:

-   Start and end time: Shows yesterday's data by default.
-   User: The current logged in user \(agents can only see their own data\).

Agents can filter and sort the information in this list to see different views, such as all of the entries for a single record or the total time worked on a record.

## Plugin

The activity timer log feature is available with the Activity Timer Reporting plugin \(sn\_activity\_timer\_reporting\). This plugin has a dependency on the Activity Timer plugin \(sn\_activity\_timer\_connected\).

**Note:** The activity timer log is not activated by default.

## Record pages with the activity timer log feature

The activity timer log feature is available on the following [record pages](csm-config-workspace-record-pages.md) in CSM Configurable Workspace:

-   CSM default record page
-   Front-line case page
-   CSM Interaction record page
-   CSM voice interaction record page
-   CSM centered chat interaction record page
-   CSM email interaction record page

