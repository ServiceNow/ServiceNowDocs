---
title: Remove a lost Sensor
description: Remove a Sensor that no longer functions or is otherwise reported as having a lost connection from the Discovery Console for OT.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Discovery Sensor for OT, Discovery Sensor for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Remove a lost Sensor

Remove a Sensor that no longer functions or is otherwise reported as having a lost connection from the Discovery Console for OT.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the Sensors page.

2.  Select the Sensor that you want to remove.

    **Danger**

    Removing Sensors in the OT environment may require working in environments with dangerous voltages, moving parts, and other safety hazards. Sensors should only be installed by persons with proper electrical and workplace safety training.

3.  Select **Actions**.

4.  Select **Remove Device from Console**.

    **Note:** The **Remove Device from Console** option is only available in the drop-down if the Device Status is **Connection Lost**.

5.  Confirm your choice to remove the Sensor.


## Result

The Sensor is no longer displayed on the Discovery Sensor for OT list page. Existing network connections associated with the Sensor remain in the system for historical purposes.

**Important:** If you remove a lost Sensor from the Console, it may still be powered on and operating at its installed location. Verify that the Sensor is properly powered down and removed from the field after removing them from the Console. If a lost Sensor is found to be operational after having been removed and must be reinstalled on the network, you must contact the Technical Support team for assistance in reconfiguring the Sensor.

