---
title: Task fields for measuring work time
description: Use default task fields to measure progress and resolution for certain records.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Default date and time fields, Date and Date/Time fields, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Task fields for measuring work time

Use default task fields to measure progress and resolution for certain records.

The following base system fields are provided on certain tables to track how long it takes to close tickets:

-   [Time worked](../../task-table/concept/c_RecordTimeWorked.md): A timer that runs when you view the record, and pauses while you close it, or when you manually pause it. Used to track the time spent by the help desk while working on the record.
-   [Resolve time](c_ResolveTime.md): A calculated field that measures the time from the moment the record is opened, to the moment the record is closed. Used to track how long it takes to resolve the record.

These fields provide different metrics for request response.

The following additional tools are available for tracking work time:

-   **Service level agreements \(SLAs\)**: Measures how long it takes a record fulfill certain conditions \(such as an incident being marked **Resolved**\).
-   **Time cards**: Use the **Time worked** field to break down how much time was spent by day of the week.

-   **[Time worked](c_TimeWorked.md)**  
The Task \[task\] table provides a time-tracking field called **Time worked**.
-   **[Resolve time](c_ResolveTime.md)**  
The **Resolve time** field is available on the Incident \[incident\] and Request \[sc\_request\] tables. This field allows for easy reporting on how long it takes for requests to be closed, and is stored as an integer number of seconds.

**Parent Topic:**[Default date and time fields](c_DefaultDateAndTimeFields.md)

