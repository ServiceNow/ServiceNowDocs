---
title: Create crews in Field Service Management
description: Create crews to assign work order tasks to a predefined group of agents.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Crew Operations, Set up workforce, Configure, Field Service Management]
---

# Create crews in Field Service Management

Create crews to assign work order tasks to a predefined group of agents.

## Before you begin

Role required: wm\_dispatcher, wm\_manager

## About this task

Crews can be defined based on the type of work needed, the geographical location, and the necessary skills. If the Territory Planning plugin is activated and the Territory model is enabled, you can pick the agents who are associated with the territories while creating a crew.

## Procedure

1.  Navigate to the **My Crews** module based on your role.

    -   Manager: Navigate to **Field Service** &gt; **Manager** &gt; **My Crews**.
    -   Dispatcher: Navigate to **Field Service** &gt; **Dispatching** &gt; **My Crews**.
2.  Click **New**.

3.  On the form, fill the fields.

4.  <table id="table_ixf_t5q_gpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the crew.

</td></tr><tr><td>

Description

</td><td>

Description of the crew.

</td></tr><tr><td>

Leader

</td><td>

Name of the crew leader.

</td></tr><tr><td>

Size

</td><td>

Total number of agents, including the leader, in the crew.**Note:** This field is mandatory.

</td></tr><tr><td>

Schedule

</td><td>

Working hours of the crew.

</td></tr><tr><td>

Location

</td><td>

Location of the crew.

</td></tr><tr><td>

Maximum Travel Radius

</td><td>

Radius in selected distance unit \(miles or kilometers\).

</td></tr><tr><td>

Distance Unit

</td><td>

Unit of distance covered in miles or kilometers

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the crew is available for selection when assigning a work order task to the crew.

</td></tr><tr><td>

From

</td><td>

Effective from the date for the crew to start work.

</td></tr><tr><td>

To

</td><td>

Effective to date for the crew to end work.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

The crew is created with the Groups, Skills, and Members related list records. If the Territory Planning plugin is activated and the Territory model is enabled, **Territory Memberships** related list appears with the list of territories associated with the crew.

