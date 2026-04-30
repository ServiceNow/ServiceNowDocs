---
title: Setting up Teams Workforce Optimization for Customer Service
description: Organize your teams into assignment groups and create reports for those groups so that you can gain visibility into the team's performance.Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate your KPI groups with assignment groups, you can monitor your team's performance.Assign one or more managers to each KPI assignment group so that they can gain visibility into the group and monitor the team's performance.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Workforce Optimization for Customer Service, Customer Service Management]
---

# Setting up Teams Workforce Optimization for Customer Service

Organize your teams into assignment groups and create reports for those groups so that you can gain visibility into the team's performance.

As an administrator, you can configure KPIs as well as child KPIs. The child KPIs appear when you drill-down into top level KPIs. For example, Closed Cases KPI has P1 Cases, P2 Cases as child KPIs.

**Parent Topic:**[Configuring Workforce Optimization for Customer Service](setup-configurable-wfo-cs.md)

## Create KPI groups to monitor team performance

Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate your KPI groups with assignment groups, you can monitor your team's performance.

### Before you begin

Role required: sn\_team\_perf.team\_performance\_admin

### About this task

By default, the KPIs that are associated with your KPI assignment groups are scheduled to collect data daily. The KPIs must have the following indicator breakdown:

-   Assignment groups
-   Assigned to

### Procedure

1.  Create a KPI group.

    1.  Navigate to **Workforce Optimization for Customer Service** &gt; **Team Performance** &gt; **KPI Groups**.
    2.  Click **New**.
    3.  In the **Name** field, enter a name for the KPI group.
    4.  In the **Type** menu, select **Teams**.
    5.  Right-click the form header and click **Save**.

        You can add up to five KPIs to a KPI group. For more information about KPIs and how the aggregates are calculated, see the overview video in the Teams example section.

2.  Add KPIs to a KPI group.

    1.  In the **KPIs** related list, click **New**.
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

You can associate a user with a primary assignment group by selecting the group in the [user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) record.

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Team Performance** &gt; **Additional Managers**.

2.  Click **New**.

3.  In the **Assignment Group** field, select an assignment group.

4.  In the **Manager** field, select a manager you want to add for this assignment group.

5.  Click **Submit**.


### What to do next

[Analyze the performance trends for your teams](teams-configurable-wfo-cs.md#).

