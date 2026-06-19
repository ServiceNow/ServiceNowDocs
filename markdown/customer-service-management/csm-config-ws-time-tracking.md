---
title: Activity timer log
description: The activity timer log feature automatically tracks the time that agents spend working on cases and interactions in CSM Configurable Workspace. The feature monitors agent activity, pauses when agents navigate away from records, and provides detailed time reports for project tracking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-config-ws-time-tracking.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Activity timer log

The activity timer log feature automatically tracks the time that agents spend working on cases and interactions in CSM Configurable Workspace. The feature monitors agent activity, pauses when agents navigate away from records, and provides detailed time reports for project tracking.

## Activity timer log overview

The activity timer log feature monitors agent activity and automatically tracks the time that agents spend working on case and interaction records. When the feature is active, agents can see the timer component in the record header. This component displays how much time has passed on the current record. The timer component can detect when an agent is actively working on a record and when the agent moves away from the tab. The timer automatically pauses when the agent navigates away from the tab and resumes when the agent returns to the tab.

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

The Time Entry table stores the start and stop events and the time captured for each start and stop pair. The system runs a scheduled job every 24 hours that aggregates this information and stores it in the Time Entry Aggregated table. Agents can view this aggregated time data in the [My Timelog list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-ws-time-tracking.md).

## Timer component

When the system administrator configures the activity timer log feature, the timer component appears in the record header next to the short description. Agents can use this timer to view the time elapsed on a record.

\[Omitted image "activity-timer-log-component.png"\] Alt text: case page with timer component

## My Timelog list

For customer service agents and consumer agents, the List view in CSM Configurable Workspace includes the **Timelog** &gt; **My Timelog** list.

-   Select **My Timelog** to view records you have worked on. The entry for each record includes these fields:

    -   User
    -   Record
    -   Record Type
    -   Short Description
    -   Start Time
    -   End Time
    -   Total Time Logged
    The **Total Time Logged** field displays the time worked for a **Start Time** and **End Time** pair. There can be multiple entries for a record.

-   Select a record in the **Record** column to open the related record form.

The **My Timelog** list includes these default filter conditions:

-   Start and end time: Yesterday's data appears by default.
-   User: The current logged-in user. Agents can only view their own data.

Agents can filter and sort the information in this list to see different views, such as all of the entries for a single record or the total time worked on a record. For more information, see the table descriptions in [Activity timer log components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activity-timer-log-components.md).

## Plugin

The activity timer log feature is available with the Activity Timer Reporting plugin \(sn\_activity\_timer\_reporting\). This plugin has a dependency on the Activity Timer plugin \(sn\_activity\_timer\_connected\).

**Note:** Activate the activity timer log before use. It is not active by default.

For more information about activating the plugin and configuring this feature, see [Configure the activity timer log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-activity-timer-log.md).

## Record pages with the activity timer log feature

The activity timer log feature is available on these [record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-record-pages.md) in CSM Configurable Workspace:

-   CSM default record page
-   Front-line case page
-   CSM Interaction record page
-   CSM voice interaction record page
-   CSM centered chat interaction record page

