---
title: Add agents to a territory
description: Add agents directly to a territory without adding them to the assignment groups. Enables agents to start working on tasks right away.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resources, Territory Planning, Set up workforce, Configure, Field Service Management]
---

# Add agents to a territory

Add agents directly to a territory without adding them to the assignment groups. Enables agents to start working on tasks right away.

## Before you begin

Role required: sn\_fsm\_tp.territory\_resource\_manager, sn\_fsm\_tp.territory\_edit\_resource\_allocation

## About this task

-   You can add agents to the territory even though its assignment group isn’t added to the territory.
-   Agents can work in a territory for the specified duration.
-   You can define multiple memberships for the same agent if they aren’t overlapping with the same start and end dates.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territories**.

2.  From the territories list, open the territory for which you want to assign agents.

3.  In the related list for the agent memberships, select **New**.

4.  On the form, fill in the fields.

<table id="table_olb_tzs_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Territory

</td><td>

Name of the territory.

</td></tr><tr><td>

Membership type

</td><td>

Agent type for territory, either as primary or secondary agent.

</td></tr><tr><td>

User

</td><td>

Name of agent.

</td></tr><tr><td>

Crew

</td><td>

Name of crew.**Note:** This field appears when the Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) plugin is activated.

</td></tr><tr><td>

From

</td><td>

Effective from the date for the agent to start work in the territory.

</td></tr><tr><td>

To

</td><td>

Effective to date for an agent to end work in territory.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The agent is added directly to a territory for the specified duration.


## Result

The agents appear in the **Agent Memberships** related list when you open the territory record. Dispatchers can then assign tasks manually or automatically to agents associated with the territory.

