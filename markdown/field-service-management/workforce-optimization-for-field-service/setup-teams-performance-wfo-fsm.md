---
title: Setting up Teams Workforce Optimization for Field Service
description: Organize your teams into assignment groups and create reports for those groups so that you can gain visibility into the team's performance.Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate KPI groups with assignment groups, you can monitor your team's performance.Assign one or more managers to each KPI assignment group so that they can gain visibility into the group and monitor the team's performance.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Workforce Optimization for Field Service, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Setting up Teams Workforce Optimization for Field Service

Organize your teams into assignment groups and create reports for those groups so that you can gain visibility into the team's performance.

You can define a set of key Performance Indicators \(KPIs\) to analyze the performance of all groups within your team. Drill into the metrics for a group, an agent, or a work order task within the team all from a central location.

As an administrator, you can configure KPIs as well as child KPIs. The child KPIs appear when you drill-down into top level KPIs. For example, Closed Work Order Tasks KPI has P1 Tasks, P2 Tasks as child KPIs.

**Related topics**  


[Teams in Workforce Optimization](using-teams-wfo-fsm.md#)

## Create KPI groups to monitor team performance

Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate KPI groups with assignment groups, you can monitor your team's performance.

### Before you begin

Role required: sn\_team\_perf.team\_performance\_admin

### Procedure

1.  Create a KPI group.

    1.  Navigate to **All** &gt; **Workforce Optimization for Field Service** &gt; **Team Performance** &gt; **KPI Groups**.

    2.  Click **New**.

    3.  In the **Name** field, enter a name for the KPI group.

    4.  In the **Type** menu, select **Teams**.

    5.  Right-click the form header and click **Save**.

        You can add up to five KPIs to a KPI group.

2.  Add KPIs to a KPI group.

    1.  In the KPIs related list, click **New**.

    2.  In the **KPI** field, select the KPI to apply for this group.

    3.  Click **Submit**.

3.  Add KPI assignment groups to the KPI group.

    **Note:**

    -   You can associate a KPI assignment group only to one KPI type.
    -   You can add additional managers to each assignment group.
    -   You can associate a user with a KPI group as the primary assignment group for that user.
    1.  In the **Assignment Groups** tab, click **Edit**.

    2.  Move the desired assignment groups from the Collection to the Assignment Groups list.

    3.  Click **Save**.


## Add managers to a KPI assignment group

Assign one or more managers to each KPI assignment group so that they can gain visibility into the group and monitor the team's performance.

### Before you begin

Role required: sn\_wfo\_admin or admin

### About this task

You can associate a user with a primary assignment group by selecting the group in the user record. For more information, see [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Field Service** &gt; **Team Performance** &gt; **Additional Manager**.

2.  Click **New**.

3.  In the **Assignment Group** field, select an assignment group.

4.  In the **Manager** field, select a manager you want to add for this assignment group.

5.  Click **Submit**.


