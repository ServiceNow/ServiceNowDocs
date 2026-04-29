---
title: Add hotspots to track custom widget performance
description: Hotspots help capture and log widget load times, which enables better debugging of long portal load times.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing portal performance, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Add hotspots to track custom widget performance

Hotspots help capture and log widget load times, which enables better debugging of long portal load times.

## Before you begin

Role required: sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widget**.

2.  Click the custom widget you want to add the hotspot to.

3.  Insert the following code snippets into the **Server script** field:

    Define a start time below the loading configuration expression:

    ```
    var startTime = new GlideDateTime();
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
    				shortDesc: '{insert a short description}'
    		});
    ```

4.  Click **Update**.


## What to do next

Open the Performance details window to view how long the custom widget takes to load data: [View widget performance metrics](view-widget-performance-metrics.md)

**Parent Topic:**[Managing portal performance](../concept/improve-manage.md)

