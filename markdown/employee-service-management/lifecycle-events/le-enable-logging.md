---
title: Enable logging for Lifecycle Events
description: Use the sn\_hr\_le.log\_level system property to enable logging for Lifecycle Events. The log entries that are generated can be used to identify errors or to acquire pertinent data about the processes that ran in a Lifecycle Events case.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Lifecycle Events logging, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Enable logging for Lifecycle Events

Use the **sn\_hr\_le.log\_level** system property to enable logging for Lifecycle Events. The log entries that are generated can be used to identify errors or to acquire pertinent data about the processes that ran in a Lifecycle Events case.

## Before you begin

Role required: admin \[sn\_hr\_le.admin\]

## Procedure

1.  Navigate to the **All** menu, and enter `sys_properties.list` in the navigation filter.

    The System Properties \[sys\_properties\] table appears.

2.  Select **Name** from the drop-down list associated with the **Search** field.

3.  In the **Search** field, enter `*sn_hr_le`.

    A list of system properties associated with Lifecycle Events appears.

4.  Select the **sn\_hr\_le.log\_level** property.

5.  Use the **Value** field to specify the option that corresponds with the type of logging you want Lifecycle Events to perform.

    |Option|Description|
    |------|-----------|
    |**NONE**|Logging is deactivated.|
    |**ERROR**|Logging is enabled. Only error logs are recorded for each Lifecycle Events case.|
    |**INFO**|Logging is enabled. Error and info logs are recorded for each Lifecycle Events case.|
    |**DEBUG**|Logging is enabled. Error, info, and debug logs are recorded for each Lifecycle Events case.|

6.  Select **Update**.


**Parent Topic:**[Lifecycle Events logging](../concept/le-logging.md)

