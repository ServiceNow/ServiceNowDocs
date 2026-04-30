---
title: Create an event rule to bind metric events to host CIs
description: Create event rules to explicitly allow binding of metric events to host CIs.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Create an event rule to bind metric events to host CIs

Create event rules to explicitly allow binding of metric events to host CIs.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Starting with the London release, Metric Intelligence no longer relies on the default Event Management binding workflow which binds nodes to host CIs. Event Management is configured to apply the default host binding algorithm when an event rule cannot find a CI to bind to, based on event data. In Metric Intelligence, with a given event rule and two different events, there can be a situation where one event binds to the correct CI and another event cannot bind. In this case, the same metric types would be created for the selected CI and for the host level CI, causing confusion.

For example: With an event rule that binds the disk percentage metric to a storage disk, one event can find a disk CI and another event cannot. This results in the disk percentage metric being created for a disk CI and for a host CI.

To avoid this confusion, Event Management default host binding is disabled for metric events in the base system. To allow host binding for metric events, explicitly create the following event rule in the Event Management event rule designer. The underlying binding functionality of the event rule designer is used to map metrics to CIs.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules** to open the event rule designer.

2.  Click **New** and ensure that the **Active** toggle switch ![Active toggle switch](../image/Active-toggle-button.png) is set to the right \(Active\).

3.  On the **Event Rule Info** tab:

    1.  Set **Source** to the data source that this rule applies to.

    2.  Enter a **Description** such as `Bind metrics at host level`.

4.  On the **Event Filter** tab, set a filter condition to indicate that **Classification** is **Metric**.

5.  Click **Save**.


**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

**Related topics**  


[Create or edit an event rule](create-or-edit-event-rule.md)

