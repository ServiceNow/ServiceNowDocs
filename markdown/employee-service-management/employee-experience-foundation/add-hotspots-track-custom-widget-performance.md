---
title: Add hotspots to track custom widget performance
description: Hotspots help capture and log widget load times, which enables better debugging of long portal load times.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-10-24"
reading_time_minutes: 1
breadcrumb: [Improve portal performance, Manage, Employee Center, Employee Service Management]
---

# Add hotspots to track custom widget performance

Hotspots help capture and log widget load times, which enables better debugging of long portal load times.

## Before you begin

Role required: sp\_admin

## About this task

-   **What are hotspots**

    Hotspots are specific areas of interest that help identify potential performance risks affecting portal load times, especially during high traffic. Logging hotspots allows users to monitor execution times for different processes and calls, including nested ones, to gain insights into what might be slowing down the user experience.

-   **When do hotspots get logged?**

    Hotspots are logged when the admin enables performance metrics and impersonates a user. Records are only collected for that session and stored in the `sn_ex_emp_fd_portal_performance_stats` table.

    To manage data volume, the system automatically deletes these records at the end of each week.


## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widget**.

2.  Click the custom widget you want to add the hotspot to.

3.  Insert the following code snippets into the **Server script** field:

    Define a start time below the loading configuration expression:

    ```
    var startTime = new GlideDateTime();
    ```

    Retrieve widget record number:

    ```
    var grInstanceRecord = $sp.getInstanceRecord();
    ```

    Retrieve widget instance identifier:

    ```
    data.spInstanceId =
                                grInstanceRecord.getUniqueValue();
    ```

    Add load time tracking:

    ```
    new sn_cd.cd_Utils().postInstanceHotspot({
    				startTime: startTime,
    				callerId: data.spInstanceId,
    				shortDesc: '{enter name of widget}'
    		});
    ```

4.  Click **Update**.


## What to do next

Open the Performance details window to view how long the custom widget takes to load data: [View widget performance metrics](view-widget-performance-metrics.md)

**Parent Topic:**[Improve portal performance](../concept/improve-manage.md)

