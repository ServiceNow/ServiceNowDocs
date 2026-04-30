---
title: Timeline pages
description: Use timeline pages to track any activity bounded by two dates, such as change request start and end dates, or incident open and close dates. Administrators can create timeline pages, which are user interactive.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Viewing record information over time, Time configuration references, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Timeline pages

Use timeline pages to track any activity bounded by two dates, such as change request start and end dates, or incident open and close dates. Administrators can create timeline pages, which are user interactive.

## Features

-   Make selected timelines available to users by role.
-   Select perspective from daily to yearly views.
-   Create dynamic labels for timeline spans.
-   Configure tooltips for each span.
-   Permit span dragging and resizing by users.
-   Lock timelines to prevent editing.

## Viewing timelines

By default, only administrators have a module to access timeline records. ITIL users can only view timelines by selecting a context menu item from an incident record.

![The timeline view, showing a green line where the current time is, and range indicators.](../image/TimelineNew.png "Timeline View")

## Administrator role users

Users with an administrator role can view timelines from the timeline page records.

1.  Navigate to **System UI** &gt; **Timeline Pages**.
2.  Select a timeline record to view.
3.  Click **View Timeline**.

## Other users

By default, timeline metrics only appear for incident records. ITIL users can view timelines associated with any task record where the metrics are set to appear as timeline records. To view the Assigned to duration and the State duration metric timelines, ITIL users can select the **Metrics Timeline** context menu UI action.

1.  Navigate to active task record, such as an incident.
2.  Right-click the banner, and select **Metrics Timeline**.

To enable non-administrators to view other timelines, [create a custom module](../task/t_MakeATimelineVisibleToASelUser.md).

-   **[Timing functionality](c_TimingFunctionality.md#)**  
Timing functionality are tools that exist to answer the question "How Long?"
-   **[Create a timeline page](../task/t_CreateATimelinePage.md)**  
Create a timeline page to track any activity bounded by two dates.
-   **[Customize the timeline page span style](../task/t_CustomizeTimelinePageSpanStyle.md)**  
The Timeline Page Span Styles related list allows you to define conditional span styles.
-   **[Timeline sub item](../task/t_TimelineSubItem.md)**  
Use the Timeline Sub Items related list to define child spans for the timeline, based on records in a table that references the parent timeline's table.
-   **[Display a metric as a timeline](../task/t_DisplayAMetricAsATimeline.md)**  
Administrators can enable users to display any metric on a timeline by activating the Timeline Metrics UI action.
-   **[Make a timeline visible to a selected user](../task/t_MakeATimelineVisibleToASelUser.md)**  
Create a custom module within an application and defining the roles that can access it, to make selected timelines available to users.
-   **[Range calculator scripts](../reference/r_RangeCalculatorScripts.md)**  
You can specify a script include that calculates range restrictions and processes parent updates in a timeline page.
-   **[Timelines](../../../use/common-ui-elements/concept/c_UsingTimelines.md)**  
Timelines display a linear calendar of tasks, such as incidents and change requests, defined by their start and end dates.

**Parent Topic:**[Viewing record information over time](../reference/r_TimeDisplay.md)

