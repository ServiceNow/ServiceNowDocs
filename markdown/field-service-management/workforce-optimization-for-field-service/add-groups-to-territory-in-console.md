---
title: Assign groups to a territory
description: Assign groups of qualifiers, dispatchers, agents, and crews to territories to optimize resource allocation for tasks.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure resources, Territory Planning, Set up workforce, Configure, Field Service Management]
---

# Assign groups to a territory

Assign groups of qualifiers, dispatchers, agents, and crews to territories to optimize resource allocation for tasks.

## Before you begin

Role required: sn\_fsm\_tp.territory\_planner, sn\_fsm\_tp.territory\_manager

## About this task

You can add qualification or dispatch groups only to an **Assignment Territory**. When you add a group to an assignment type of territory, the system automatically updates the relevant assignment groups, adding the group members to the territory.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  In the Territories panel, select the desired territory.

    The territory record appears.

3.  Select the **Qualification Groups** tab or **Dispatch Groups** tab and click **Add**.

4.  On the form, fill in the fields.

<table id="table_olb_tzs_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group

</td><td>

Enter the name of the group responsible for qualifying and dispatching work orders or tasks.

</td></tr><tr><td>

Membership type

</td><td>

Choose the membership type—either primary or secondary. This determines the priority for assignments if the group is part of multiple territories. For example, assign a primary membership to the group for one territory and a secondary membership for another.

**Note:** This field is evaluated only for assignment groups.

</td></tr><tr><td>

Territory

</td><td>

Enter the name of the territory to map to the group.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the group is available for scheduling.

</td></tr></tbody>
</table>5.  Select **Save**.

    A group is added to the territory.


## Result

Once a qualification or dispatch group is added to a territory, the system automatically updates the associated assignment groups, adding the group members to the territory. Whether it's a qualification or dispatch group, the system displays them into the respective related lists, simplifying the reference process when handling territories.

