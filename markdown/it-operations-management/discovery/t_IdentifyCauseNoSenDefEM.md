---
title: Find the cause of a "No Sensor Defined" error message
description: Every active probe looks for a corresponding sensor to process the data that is collected by the probe. The "No Sensors Defined" message indicates that the corresponding sensor for the probe is missing or inactive.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-06-05"
reading_time_minutes: 1
breadcrumb: [Discovery error messages, Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Find the cause of a "No Sensor Defined" error message

Every active probe looks for a corresponding sensor to process the data that is collected by the probe. The "No Sensors Defined" message indicates that the corresponding sensor for the probe is missing or inactive.

## Before you begin

Role required: sn\_cloud\_ops\_ws.cloud\_ops\_admin or admin

## About this task

To find the cause of this error, identify the **Short Message** field of the error record. This field shows the name of the probe for which the sensor is missing.

## Procedure

1.  Depending on the application you're using, do one of the following:

    -   To identify the cause of the error using Cloud Discovery Workspace, navigate to **Cloud Discovery Workspace** &gt; **Cloud Discovery** &gt; **Diagnostics** &gt; **Discovery Log**.
    -   To identify the cause of the error using Discovery, navigate to **All** &gt; **Discovery** &gt; **Output and Artifacts** &gt; **Discovery Log**.
2.  Filter the **Level** column by **Error**.

    If you are using Discovery, you can also view the Error Report on the Discovery dashboard.

3.  Note the **Short Message** field of the error record.

    This field shows the name of the sensor where the error has occurred.


**Parent Topic:**[Discovery error messages](../concept/c_DiscoveryErrorMessages.md)

**Related topics**  


[Find the cause of a sensor error message](t_FindTheCauseOfASensorErrorMessage.md)

[Fix the cause of a sensor error message](t_FixTheCauseOfASensorErrorMessage.md)

[Find the cause of a "Probe not found" error](t_FindTheCauseOfAProbeNotFoundError.md)

