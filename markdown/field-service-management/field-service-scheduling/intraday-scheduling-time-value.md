---
title: Change the value for agents being considered early or late
description: Change the value that determines whether an agent is early or late.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Intraday schedule automation, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Change the value for agents being considered early or late

Change the value that determines whether an agent is early or late.

## Before you begin

Role required: admin

## About this task

By default, agents are considered early or late if they’re 30% early or late from the specified time. For example, if an agent is 18 minutes late to a one-hour task would be 30% late. You can change this percentage value. You can also switch from using a percentage to using minutes.

**Warning:** Don’t change any values related to the conditions or check types. Doing so will break the flows.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Work order task progressed** flow.

3.  Set the value to minutes by entering a minutes value and setting the percentage value to 0.

4.  Set a different percentage by changing the percentage value.

    **Note:** Percentage is prioritized over minutes. If the percentage fields have a value other than 0, then percentage is used as the value even if a minutes value has been set.

5.  Select **Save**.


