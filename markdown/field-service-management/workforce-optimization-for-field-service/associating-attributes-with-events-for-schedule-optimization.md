---
title: Associating attributes with events for Schedule Optimization
description: Schedule Optimization auto-assigns tasks and adapts to changing conditions by following policies to optimize travel time and agent availability. When Workforce Optimization for Field Service is activated, you can associate attributes to events, enhancing optimization and overall scheduling accuracy.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workforce Optimization, Set up workforce, Configure, Field Service Management]
---

# Associating attributes with events for Schedule Optimization

Schedule Optimization auto-assigns tasks and adapts to changing conditions by following policies to optimize travel time and agent availability. When Workforce Optimization for Field Service is activated, you can associate attributes to events, enhancing optimization and overall scheduling accuracy.

## Agent Schedule Attributes Table

<table id="table_gkt_1z4_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent schedule

</td><td>

Reference to event

</td></tr><tr><td>

Agent schedule occurrence date

</td><td>

Date when agent event occurs

</td></tr><tr><td>

Agent Schedule occurrence date span

</td><td>

Schedule span of agent eventThe span can't exceed 30 days.

</td></tr><tr><td>

Actual agent schedule

</td><td>

Reference to actual agent event

</td></tr><tr><td>

Schedule Status

</td><td>

Status of the event.Events can be marked as either **optional** or **mandatory**:

-   Optional Events: The technician is free during these times and can be assigned tasks.
-   Mandatory Events: The technician is busy during these times and can’t be assigned tasks.

</td></tr><tr><td>

Location

</td><td>

Location for the agent event

</td></tr><tr><td>

Travel duration

</td><td>

Estimated travel duration to event

</td></tr><tr><td>

Travel home duration

</td><td>

Estimated travel home duration from event

</td></tr></tbody>
</table>## Rest APIs

The data within the table will be inserted via two REST APIs.

-   Create event with attributes: Use this resource to create events with attributes such as location, schedule status.
-   Edit event with attributes: Use this resource to associate attributes to existing events.

You can use scripted REST APIs to create or edit events, including their attributes. You can also use scripted REST APIs to override a technician's **Planned Break**. For more information on REST APIs, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB2328246](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2328246)

## Scenarios

-   Mandatory events: When an event is marked as **Mandatory**, the Schedule Optimization Engine adjusts the Technician’s schedule based on this event attributes. The engine accounts for travel time to and from the event location, ensuring seamless integration with adjacent tasks/events.
-   Optional events: When an event is marked as **Optional** it is treated as available time slot for the technician. The event is excluded from the optimization process and is not sent to the Schedule Optimization engine.
-   Flexible break override: When the flexible break constraint is enabled and a planned break is overridden using the Actual Break option, the **Actual Break** details are sent to the Schedule Optimization engine. The **Planned Break** window is released and becomes available for task scheduling.

Schedule Optimization calculates the travel duration to the event and from the event to the technician's home location during an optimization run, based on the configured travel estimate provider.

**Related topics**  


[Configuring Schedule Optimization](schedule-optimization-engine.md)

