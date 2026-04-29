---
title: Example – Multiple time zones for dispatchers
description: Explore how adding multiple time zones to Dispatcher Workspace makes managing agent schedules more efficient.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Time Zones, Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Example – Multiple time zones for dispatchers

Explore how adding multiple time zones to Dispatcher Workspace makes managing agent schedules more efficient.

## About this task

Problem scenario: Sarah is a ServiceNow administrator for a European field service company. Dispatchers in their organization face the daily challenge of scheduling field service agents who are based in all the time zones across Europe. Because dispatchers can’t see what time zones agents are in, dispatchers regularly assign urgent work order tasks to agents in the wrong time zone. Improper work order assignment leads to delays in completing the work and customer dissatisfaction.

Solution: Sarah decides to add all the time zones that field service agents are located in as options for dispatchers to add to their Dispatcher Workspace. Switching between all the time zones agents are located in to see local times significantly enhances dispatcher's ability to manage and schedule field service agents effectively. With immediate visibility into the local times of agents, dispatchers can make informed decisions, ensuring that no agent is dispatched at an inconvenient local time. All Sarah had to do was add the relevant time zones to the dispatcher’s user record. This streamlined the scheduling processes, reduces errors, and led to higher customer satisfaction.

## Before you begin

Role required: admin

Time zones for dispatchers example 

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User**.

2.  Select a user who’s a dispatcher in Europe.

3.  Select and hold \(or right-click\) **Time zone** and select **Configure Dictionary**.

4.  Select the **Choices** list.

5.  Set the **Inactive** column to **false** for the following time zones:

    1.  Europe/ Dublin
    2.  Europe/ Amsterdam
    3.  Europe/ Athens
    4.  Europe/ Istanbul
6.  Select **Update**.

    The dispatcher Sarah selected can now add any of the four European time zones to their Dispatcher Workspace.


**Related topics**  


[Configure multiple time zones for dispatchers](add-remore-time-zones.md)

[Change the time zone in Dispatcher Workspace](change-timezone-calendar.md)

