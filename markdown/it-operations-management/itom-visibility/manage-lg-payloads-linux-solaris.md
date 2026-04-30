---
title: Manage large storage payloads in Linux and Solaris
description: Large payloads for Linux and Solaris direct attached storage can cause out of memory errors if not configured to serialize the processing of the payload.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Manage large storage payloads in Linux and Solaris

Large payloads for Linux and Solaris direct attached storage can cause out of memory errors if not configured to serialize the processing of the payload.

## Before you begin

Role required: discovery\_admin or admin

## About this task

When Linux or Solaris storage sensors process payloads from large disk arrays, worker threads run simultaneously and can run an instance node out of memory, requiring a restart. To prevent this, the \[discovery\_sensor\_yield\] table controls the behavior of worker threads used to process large payloads. When Discovery processes a sensor, it checks the \[discovery\_sensor\_yield\] table for that sensor. If the sensor is listed in the table, and if the payload size exceeds the configured limit in the table, then the worker attempts to secure a lock before processing the payload. If the lock is not available because another worker is already processing a large payload, the waiting worker re-schedules the next job for 30 seconds later and moves on to other tasks. The job then waits in the Schedule Item \[sys\_trigger\] table for an idle worker to pick it up. This serialization occurs per node, enabling multiple nodes to process large payloads simultaneously. The processing interval of 30 seconds is not configurable.

**Important:** These threshold values were created for Linux and Solaris storage sensors only and, in most cases, should not be changed. If your instance is running out of memory while simultaneously processing multiple, large storage payloads, consider scheduling Discovery of these systems to times of lower activity. If this is not possible, examine the ECC queue to determine which storage sensor might be causing the issue and note the size of the payload. If the payload size is below that of the threshold in the \[discovery\_sensor\_yield\] table, lower the threshold value enough to serialize that payload. If a sensor other than the Linux or Solaris storage sensor is responsible, you can add that sensor to the \[discovery\_sensor\_yield\] table. Make sure to set the threshold value correctly for the payload size. Serializing sensor processing can slow Discovery.

## Procedure

1.  In the application navigator filter, enter **discovery\_sensor\_yield.list**.

    The base Discovery system serializes these sensors when their payloads exceed 512 KB:

    -   **Solaris - Storage**
    -   **Linux - Storage**
    -   **Unix - ADM Enhanced**
    -   **Windows - ADM Enhanced**
2.  To change the threshold, double-click in the **Value** column in the list and edit the size.

    ![Editing the sensor yield threshold](../image/DiscoverySensorYield.png "Editing the sensor yield threshold")

3.  To add another sensor and configure it for payload serialization, click **New** and complete the fields in the form.

    -   **Sensor**: Storage sensor to configure.
    -   **Value**: Threshold size for the sensor.
4.  Click **Submit**.


**Parent Topic:**[Storage discovery](../concept/c_Storage.md)

