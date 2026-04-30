---
title: View alerts in the flapping state
description: You can view alerts that are specifically in the flapping state.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View alert information, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View alerts in the flapping state

You can view alerts that are specifically in the flapping state.

## Before you begin

Before starting this procedure, ask your administrator to configure alert flapping properties.

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

Flapping occurs when the event source continues to generate events even after its associated alert has been closed. Flapping causes the resource's status to repeatedly fluctuate between the **OK** severity and a severity requiring attention, for example, **Critical**.

The frequency of events from an identical source within a given time interval determines whether an alert is in a flapping state or a new issue has occurred. Based on the **evt\_mgmt.flap\_frequency** and **__evt\_mgmt.flap\_interval__** property values:

-   If the same issue is recurring, Event Management associates the new event with the existing alert and the state of the alert is set to **Flapping**.
-   If the issue occurs after the time interval expires, Event Management creates an alert.

For example, you can respond to an alert by rebooting a problematic server. After no events are generated for several minutes, it is assumed that the issue is fixed and the alert is closed. If the reboot did not actually fix the issue, this server can generate more events later. Then additional alerts are generated for the same issue.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Click the number of an alert that is in the **Flapping** state.

3.  On the alert, click the **Flapping** tab.

    |Field|Description|
    |-----|-----------|
    |**Flapping tab**|
    |Flap count|The number of times the alert has flapped—that is, has fluctuated between a closed and a non-closed state—within the flap interval since the start time in the **Flap start window**.|
    |Flap start window|The initial start time to measure the flapping occurrences.|
    |Flap last update time|The last time flapping occurred. This time is the platform processing time, not the source system time.|
    |Flap last state|The state before the alert entered the flapping state.|

4.  If the **Parent** field is empty, address this alert as a new issue.


**Parent Topic:**[View alert information](t_EMViewAlert.md)

**Related topics**  


[Configure alert flapping](t_EMConfigAlertStateFlapDetect.md)

