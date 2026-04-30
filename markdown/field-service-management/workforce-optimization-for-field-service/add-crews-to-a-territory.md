---
title: Add crews to a territory
description: Add crews directly to territories, allowing members from your territories to join crews instantly and handle tasks immediately.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring resources for territories, Configuring Field Service Territory Planning, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Add crews to a territory

Add crews directly to territories, allowing members from your territories to join crews instantly and handle tasks immediately.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## About this task

To work with crews in territories, you need to activate the Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) plugin.

The following are the two ways to create crews:

1.  Manual: You can hand-pick agents from any territory you're a member of to form a crew. It's like assembling your own team for a specific job.
2.  Automatic: Dynamic scheduling handles automatic crew creation. When dynamic scheduling is selected as a scheduling method, the system can create crews on its own when they're needed, saving you time and effort. It does this by pulling agents from the territory linked to the specific work order task, ensuring the right people are assigned to the right job.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territories**.

2.  From the territories list, open the territory for which you want to assign crews.

3.  Assign a crew for the territory.

    -   Select an existing crew.
    -   Create a new crew by selecting **New** in the crew memberships related list.
4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the crew.|
    |Description|Description of the crew.|
    |Leader|Name of the crew leader.|
    |Size|Total number of agents, including the leader, in the crew.|
    |Schedule|Working hours of the crew.|
    |Location|Location of the crew.|
    |Maximum Travel Radius|Radius in selected distance unit \(miles or kilometers\).|
    |Distance Unit|Unit of distance covered in miles or kilometers|
    |Active|Option to indicate whether the crew is available for selection when assigning a work order task to the crew.|
    |From|Effective from the date for the crew to start work.|
    |To|Effective to date for the crew to end work.|

5.  Select **Submit**.

    The crew is added directly to a territory for the specified duration.


## Result

The crew becomes visible within the **Crew Memberships** related list of the territory record.

## What to do next

Dispatchers can assign crews to work order tasks. For more information, see [Assign work order tasks to crews](assign-wot-crew-operations.md).

