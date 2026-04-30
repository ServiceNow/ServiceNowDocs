---
title: Configure alert flapping
description: Set flapping properties to determine when an alert enters and exits the flapping state. Flapping can indicate configuration problems \(that is, thresholds set too low\), troublesome services, or real network problems.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Alert lifecycle configuration, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure alert flapping

Set flapping properties to determine when an alert enters and exits the flapping state. Flapping can indicate configuration problems \(that is, thresholds set too low\), troublesome services, or real network problems.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Flapping occurs when the event source continues to generate events even after its associated alert has been closed. Flapping causes the resource's status to repeatedly fluctuate between the **OK** severity and a severity requiring attention, for example, **Critical**.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Event Management Properties**.

2.  Edit the following properties, as appropriate.

<table id="choicetable_ofd_yxs_xtb"><thead><tr><th align="left" id="d537668e94">

Property

</th><th align="left" id="d537668e97">

Description

</th></tr></thead><tbody><tr><td id="d537668e103">

**evt\_mgmt.update\_alert\_restricted\_fields\_elapsed\_time**

</td><td>

When the system receives events that do not update alerts—because the event data is not new and is identical to the existing alert—system fields are not updated by default. This helps reduce noise. For example, a "keep alive" event might be sent every few minutes from a server to confirm that a device is still connected, even if no new data is being exchanged.

 This property defines the minimum time interval \(in seconds\) that must pass before an alert can be updated based on identical events.

 If an identical event is received within this interval, the update is suppressed to avoid generating frequent, redundant notifications. By default, the interval is set to 86,400 seconds \(24 hours\).

</td></tr><tr><td id="d537668e121">

**evt\_mgmt.flap\_interval**

</td><td>

Flap interval, in seconds, which is the time period within which an alert enters the flapping state.

 An alert enters the flapping state when its current **Flap Count** value reaches or exceeds the given **evt\_mgmt.flap\_frequency** property value within the time period specified by the **__evt\_mgmt.flap\_interval__** property.

</td></tr><tr><td id="d537668e146">

**evt\_mgmt.flap\_frequency**

</td><td>

Flap frequency, frequency an alert must reoccur to enter the flapping state.

</td></tr><tr><td id="d537668e155">

**evt\_mgmt.flap\_quiet\_interval**

</td><td>

Flap quiet interval \(in seconds\), quiet time that must pass for an alert to exit the flapping state.An alert exits the flapping state when the time interval between the latest occurrence of the event and the **Flap last update time** of the alert reaches or exceeds the **__evt\_mgmt.flap\_quiet\_interval__** property value. An alert can also exit flapping in these conditions:

 -   When an incoming event arrives after the **flap\_quiet\_interval** time has elapsed. The new alert generates and its state value depends on the incoming event severity.
-   After a background job, which runs every five minutes, verifies that no alert updates occurred and the **flap\_quiet\_interval** time has elapsed. If there are no updates, the alert shows the previous state value that it had before the background job ran.


</td></tr></tbody>
</table>3.  Click **Save**.


## What to do next

You can monitor the **Event Management** &gt; **All Alerts** list for alerts that are in the flapping state. For details, see [View alerts in the flapping state](t_EMViewAlertFlapping.md).

**Parent Topic:**[Alert lifecycle configuration](../concept/c_EMAlertRule.md)

**Related topics**  


[Work with flapping alerts](../../event-management-operator/task/operator-handle-alerts-flapping.md)

[View alerts in the flapping state](t_EMViewAlertFlapping.md)

