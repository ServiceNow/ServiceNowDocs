---
title: Configure the security event ribbon
description: Configure the security event ribbon on the Instance Security Center homepage to include only those events that are relevant for tracking instance security in your operations. You can also change the order in which the security event tiles appear on the ribbon.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor security events, Instance Security Center, Platform Security]
---

# Configure the security event ribbon

Configure the security event ribbon on the Instance Security Center homepage to include only those events that are relevant for tracking instance security in your operations. You can also change the order in which the security event tiles appear on the ribbon.

## Before you begin

Role required: security\_dashboard\_user or admin

## About this task

The security event ribbon is initially populated with a full set of standard security events. You can customize it by removing the events that are not relevant to your organization.

-   For example, if you suspect that security issues are due to the actions of internal personnel, include the Admin Logins, Admin Users added, and Security Elevations event indicators.
-   These indicators monitor how many times users with admin roles attempted to log in and, if admin users were added, what attempts were made to elevate security roles.

**Note:** To learn about the types of security events that appear in the event ribbon, see [Monitor security events](../concept/instance-sec-center-event-ribbon.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Instance Security Center**.

2.  In the event ribbon, click **Edit** \(![Events ribbon Edit button](../image/isc-events-ribbon-edit.png)\).

    On the Edit Events form, the **Selected** column contains the events that are already listed.

3.  To add security events to the event ribbon, move them from the **Available** column to the **Selected** column.

    To change the order the events appear on the ribbon, select an event, then click the up or down arrow to move it to its correct position.

    -   Place the events in the same sequential order they should appear on the Instance Security Center event ribbon.
    -   The events you place at the top of the **Available** column appear sequentially, beginning on the left side of the Instance Security Center event ribbon. The events placed towards the bottom of the column appear on to the right on the event ribbon.
4.  To remove security events from the event ribbon:

    -   In the **Selected** column, select the security events that you want to remove from the event ribbon.
    -   Move them from the **Selected** column to the **Available** column.
5.  Click **Save**.


**Parent Topic:**[Monitor security events](../concept/instance-sec-center-event-ribbon.md)

**Related topics**  


[Instance Security Center](../concept/instance-security-center.md)

