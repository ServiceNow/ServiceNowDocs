---
title: Schedule Optimization for Planned Crews
description: Use Schedule Optimization to assign tasks efficiently to planned crews, ensuring alignment with crew schedules and locations.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Schedule Optimization for Planned Crews

Use Schedule Optimization to assign tasks efficiently to planned crews, ensuring alignment with crew schedules and locations.

There are two types of crews in Field Service Management:

-   **Planned crews**: Created in advance with assigned members, schedules, and locations. These crews are ideal for predictable work patterns and structured team assignments.
-   **Dynamic crews**: Created on demand by the system to fulfill specific tasks. These crews are flexible but not compatible with Schedule Optimization.

Schedule Optimization supports task assignment only for **planned crews**, which are pre-created groups of agents with defined schedules and locations. It does **not** support **dynamic crews**, which are formed automatically based on task requirements and agent availability.

To enable Schedule Optimization for planned crews:

-   [Activate the Crew Operations for Field Service](activate-fsm-crew-scheduling.md) plugin.
-   [Create planned crews](create-crews-fsm.md) in the system.
-   Ensure each planned crew is assigned a specific **location** and **schedule**.

These steps ensure that the optimization engine can accurately match tasks to available crews based on time and geography.

