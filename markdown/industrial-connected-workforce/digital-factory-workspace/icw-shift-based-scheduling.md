---
title: Shift-based scheduling for manufacturing standards
description: Shift-based scheduling enables you to create schedule plans that automatically generate standard tasks aligned with your factory's shift patterns and production day configurations. In shift-based scheduling, you don't have to specify precise start and end date-time values manually.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Industrial Standards, Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Shift-based scheduling for manufacturing standards

Shift-based scheduling enables you to create schedule plans that automatically generate standard tasks aligned with your factory's shift patterns and production day configurations. In shift-based scheduling, you don't have to specify precise start and end date-time values manually.

## Overview of shift-based scheduling

Manufacturing standard tasks are planned activities that must be released in alignment with operational shift schedules. Previously, creating a custom schedule requires you to align the start and end date-time settings with shift time frames precisely. Any misalignment can cause errors in task generation, causing scheduling failures and operational delays.

Shift-based scheduling enables you to address these challenges by using the shift configuration defined for the functional location. In shift-based scheduling, the system automatically calculates when tasks must be generated, released, and expired. You are only required to select a start date and one or more shifts.

## How shift-based scheduling works

When you create a shift-based schedule plan, the system follows a shift-first logic to generate tasks:

1.  Shift selection: You select which shifts the schedule applies to. The available shifts are determined by the industrial shift configuration associated with the functional location of the manufacturing standard. The shift selection is positioned at the top of the custom schedule modal, so you define whether the schedule is shift-based before setting up the recurrence pattern.
2.  Start date: You specify the date from which the schedule begins releasing tasks. You do not need to specify a time. The system uses the shift start times to determine when tasks are released.
3.  Sequential task generation: The system generates tasks one shift at a time rather than all at once. For each scheduled date, the system checks whether the schedule is active and creates tasks for each selected shift according to the shift's defined boundaries.
4.  Timezone application: The system applies the factory timezone from the location record linked to the functional location's site to ensure that shift times are interpreted correctly.
5.  Automatic timeframe calculation: The system calculates the start and end timeframes for each task based on the production day configuration of the functional location as defined in the industrial shift configuration.

## Task lifecycle management

Shift-based scheduling includes automated task lifecycle management to ensure data integrity and reduce clutter:

-   Task release: Tasks are released at the start of each selected shift on the scheduled dates, according to the recurrence pattern defined in the schedule plan.

    You can also set an offset on a schedule plan. An offset determines the how much time in advance the task is generated in relation to planned start.

    The default offset time is 1 hour. For example, a task is planned to start at 20:00. Based on the default offset of 1 hour, Task is generated 19:00.

-   Task expiration: Tasks expire according to the expiration setting on the standard in relative to the planned start time.
-   Duplicate prevention: The system detects and cleans up duplicate events and tasks during schedule updates, ensuring that only valid, non-duplicated tasks are present.
-   Schedule changes: When a schedule plan is deactivated, modified, or has its shift configuration updated, the system invalidates pending occurrence checks and adjusts future task generation accordingly.

## Benefits of shift-based scheduling compared to non-shift based scheduling

|Feature|Shift-based scheduling|Non-shift based scheduling|
|-------|----------------------|--------------------------|
|Date-time configuration|Only a start date is required. Start and end times are automatically calculated from the shift configuration.|Requires precise start and end date-time values that must align with the intended schedule window.|
|Task generation|Tasks are generated sequentially, one shift at a time, based on the selected shifts and production day configuration.|Tasks are generated based on the configured date-time range and recurrence pattern.|

## Prerequisites for shift-based scheduling

Make sure you have set up the following prerequisites before using shift-based scheduling:

-   Industrial shift configurations are defined for the functional location associated with the manufacturing standard. For more information about configuring shifts, see [Define a shift](../task/define-shifts.md).
-   The site location record linked to the functional location has a timezone defined.
-   The manufacturing standard is published and is associated with a functional location that has shift configurations.

## Scheduling quality inspection standards for shifts

As a line leader at a food and beverage manufacturer, you spend 30 minutes setting up shift schedules for quality inspection standards. You may encounter frequent errors when timeframes don't align with shift boundaries, which requires multiple attempts.

With shift-based scheduling, you may be able to complete the same scheduling in under 5 minutes:

1.  Open the manufacturing standard and navigate to the **Scheduled Plans** tab.
2.  Select **New schedule** and then **Custom schedule**.
3.  Enable the shift option at the top of the custom schedule modal.
4.  Select the morning, afternoon, and night shifts.
5.  Set the start date to the beginning of the next work week.
6.  Verify the factory timezone is correctly applied.
7.  Configure a daily recurrence pattern and saves the schedule.

The system automatically generates inspection tasks for each shift on each scheduled day. Tasks are released at the start of each shift and expire at the end of the shift window if not completed.

**Parent Topic:**[Exploring Industrial Standards](../reference/industrial-standards-landing-page.md)

