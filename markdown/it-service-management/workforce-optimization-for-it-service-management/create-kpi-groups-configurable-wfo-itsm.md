---
title: Create KPI groups to monitor team performance
description: Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate your KPI groups with assignment groups, you can monitor your team's performance.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up, Teams, Workforce Optimization for ITSM, IT Service Management]
---

# Create KPI groups to monitor team performance

Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate your KPI groups with assignment groups, you can monitor your team's performance.

## Before you begin

Role required: sn\_team\_perf.team\_performance\_admin

## About this task

By default, the KPIs that are associated with your KPI assignment groups are scheduled to collect data daily. The KPIs must have the following indicator breakdown:

-   Assignment groups
-   Assigned to

## Procedure

1.  Create a KPI group.

    1.  Navigate to **Workforce Optimization for ITSM** &gt; **Team Performance** &gt; **KPI Groups**.

    2.  Click **New**.

    3.  In the **Name** field, enter a name for the KPI group.

    4.  In the Type menu, select **Teams**.

        **Note:** If you select a type that isn’t supported in Team Performance, such as the Channels type, the Related list for the KPI group will show the default list from the sn\_team\_perf\_kpi\_group\_m2m\_pa\_indicators table.

    5.  Right-click the form header and click **Save**.

        You can add up to five KPIs to a KPI group. For more information about KPIs and how the aggregates are calculated, see the overview video in the [Teams example](../concept/example-team-reporting-configurable-wfo-itsm.md) section.

2.  Add KPIs to a KPI group.

    1.  In the KPIs related list, click **New**.
    2.  In the **KPI** field, select the KPI to apply for this group.
    3.  Click **Submit**.
3.  Add KPI assignment groups to the KPI group.

    **Note:**

    -   You can associate multiple KPI groups with one or more assignment groups.
    -   You can add additional managers to each assignment group.
    -   You can associate a user with a KPI group as the primary assignment group for that user.
    1.  In the **Assignment Groups** tab, click **Edit**.
    2.  Move the desired assignment groups from the Collection to the Assignment Groups list.
    3.  Click **Save**.
    **Note:** When you open a KPI Group, by default, the KPI Groups form displays the KPI Group's type based on the application you’ve currently selected.


**Parent Topic:**[Setting up Teams in Workforce Optimization for ITSM](../concept/setup-teams-configurable-workforce-optimization-itsm.md)

