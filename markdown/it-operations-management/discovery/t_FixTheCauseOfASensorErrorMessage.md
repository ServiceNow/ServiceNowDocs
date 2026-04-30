---
title: Fix the cause of a sensor error message
description: To fix a Discovery sensor error message, you must fix the JavaScript file containing the code that generated the error.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Discovery error messages, Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Fix the cause of a sensor error message

To fix a Discovery sensor error message, you must fix the JavaScript file containing the code that generated the error.

## Before you begin

Role required: admin

## About this task

To fix the JavaScript file:

## Procedure

1.  Navigate to the module in Discovery in which the error occurred.

    In this example, navigate to **Discovery Definition** &gt; **Script Includes**.

2.  Fix the error.

    1.  In this example, search for DiscoverySmiFcSwitchSensor in the **Name** field.

        ![Discovery script includes](../image/DiscoverySensorStackTraceJavaScript.png "Discovery script includes")

    2.  Click on the link to go to the details page for that script include.

    3.  Modify the JavaScript script on that page to fix the error indicated.

    4.  Click **Update**.


**Parent Topic:**[Discovery error messages](../concept/c_DiscoveryErrorMessages.md)

**Related topics**  


[Find the cause of a sensor error message](t_FindTheCauseOfASensorErrorMessage.md)

[Find the cause of a "No Sensor Defined" error message](t_IdentifyCauseNoSenDefEM.md)

[Find the cause of a "Probe not found" error](t_FindTheCauseOfAProbeNotFoundError.md)

