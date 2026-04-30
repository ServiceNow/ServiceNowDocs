---
title: Change the time that determines whether an agent has acted
description: Fine-tune the amount of time that determines whether an agent has acted when scheduled.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Intraday schedule automation, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Change the time that determines whether an agent has acted

Fine-tune the amount of time that determines whether an agent has acted when scheduled.

## Before you begin

Role required: admin

## About this task

The Agent Not Take Action flow is made up of three subflows that determine whether an agent acted when scheduled to based on the time values.

**Warning:** Don’t change any values related to the conditions or check types. Doing so breaks the flows.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Choose the subflow that you want to edit.

    -   FSM wait for travel start.

    -   FSM wait for work complete.

    -   FSM wait for work start.

3.  Select the action **Wait for 30 minute\(s\) after**.

4.  Change the value from 30 to the new value.

5.  Select **Save**.


