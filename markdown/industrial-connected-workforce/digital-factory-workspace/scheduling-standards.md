---
title: Scheduling standards
description: Scheduling of standards and tasks enables a proactive planning approach in manufacturing.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Industrial Standards, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Scheduling standards

Scheduling of standards and tasks enables a proactive planning approach in manufacturing.

This feature enables equipment owners and operators in manufacturing environments to plan and schedule all operational standards needed to maintain optimal equipment conditions. It replaces manual, spreadsheet-based planning with a centralized approach to task management. By doing so, it helps bring together planning activities that were previously spread across different systems.

The system offers flexible scheduling options. You can set up daily, weekly, and monthly tasks, including more complex patterns such as "every Tuesday of every other week." This helps align maintenance and operational standards with how the equipment is used.

By automatically creating tasks based on predefined standards, the feature helps reduce the mental effort required from operators. Instead of having to remember or track tasks manually, operators receive system prompts, which helps make sure that no critical tasks are missed.

The following rules exist for event scheduling:

-   Users with the **sn\_icw.admin** role can configure the property **sn\_icw\_std.scheduled\_creation\_minutes\_offset**, which specifies how much ahead of the specified time the scheduled tasks should be created.
-   The planned start and planned end are automatically set according to the schedule.
-   The shift must be part of the production day.
-   For custom schedules, the period when the schedule is active is determined by the overlap between the recurrence pattern and the time span allocated for shifts.

## Shift-based scheduling

Shift-based scheduling provides a simplified approach to scheduling manufacturing standard tasks for shifts:

-   You can select shifts before configuring the recurrence pattern. The shift selection is positioned at the top of the custom schedule modal, which streamlines the setup flow.
-   You only need to select a start date. The system automatically calculates the start and end timeframes for task generation based on the selected shifts and the production day configuration of the functional location.
-   The **Start date/time** and **End date/time** fields are hidden when shift-based scheduling is enabled, because the system derives these values from the shift configuration.
-   Tasks are generated sequentially, one shift at a time, aligned with shift boundaries. This shift-first logic ensures that tasks are accurately created for each selected shift.
-   Tasks that are not completed within the designated shift window are automatically expired and removed, keeping operator dashboards clean.
-   Duplicate events and tasks are detected and cleaned up during schedule updates, maintaining data integrity.

-   **[Scheduling calendar](calendar-view-scheduling.md)**  
The calendar view provides a visual interface for scheduling manufacturing tasks. It helps operators and line leaders plan, view, and manage task schedules more easily by showing occurrences, overlaps, and exceptions in a familiar calendar format.
-   **[Create a standard schedule plan](../task/create-events-based-on-schedules.md)**  
Create a plan for the scheduled creation of standard tasks.

**Parent Topic:**[Using Industrial Standards](using-industrial-standards.md)

