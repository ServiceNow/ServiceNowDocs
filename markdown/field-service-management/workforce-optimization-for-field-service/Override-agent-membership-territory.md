---
title: Modify the resource membership of agents or crews associated with a territory
description: Modify the territory membership of agents or crews to make them available to work in a territory for a certain period, set their priority when assigning tasks, or mark them as inactive.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring resources for territories, Configuring Field Service Territory Planning, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Modify the resource membership of agents or crews associated with a territory

Modify the territory membership of agents or crews to make them available to work in a territory for a certain period, set their priority when assigning tasks, or mark them as inactive.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner

## About this task

All agent and crew resources in the assignment group associated with a territory are available to work in that territory by default. You can modify their membership by making them inactive to avoid assigning tasks to them or set their territory membership type to either primary or secondary. Resources with a primary membership are prioritized over resources with a secondary membership when assigning tasks.

**Note:**

-   You can customize the membership of any resources regardless their assignment group and assignment territory.

-   You must activate Field Service Crew Operations plugin to view and customize crew membership. For more information, see [Activate Field Service Crew Operations](activate-fsm-crew-scheduling.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  In the Territories panel select the territory.

    The territory record appears.

3.  Modify the desired membership.

    -   To modify agent membership, select **Agent Membership** tab.
    -   To modify crew membership, select **Crew Membership** tab.
4.  Select **Add**.

5.  On the form, fill in the fields.

<table id="table_rtc_c5g_ttb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Territory

</td><td>

Name of the territory.This field is automatically set to the territory for which the agent or crew is a member.

</td></tr><tr><td>

User

</td><td>

Name of the agent whose membership you want to change.This field is available only when a crew is not selected in the **Crew** field.

</td></tr><tr><td>

From

</td><td>

Date from which the resource is available to work in the territory.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the resource is available to work in the territory.

</td></tr><tr><td>

Membership type

</td><td>

Type of membership for the resource, either primary or secondary. For example, if a resource is part of two territories simultaneously, assign a primary membership to the resource for territory one and a secondary membership for the other territory.

</td></tr><tr><td>

Crew

</td><td>

Name of the crew whose membership you want to change.This field is available only when an agent is not selected in the **User** field.

</td></tr><tr><td>

To

</td><td>

Date until which the resource is available to work in the territory.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

The agent or crew availability and membership is modified.

