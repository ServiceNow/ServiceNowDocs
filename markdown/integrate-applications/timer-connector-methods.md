---
title: Timer connector methods
description: Learn about the Timer connector methods and event.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Timer, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Timer connector methods

Learn about the Timer connector methods and event.

## Start method

The Start method enables you to set a time in milliseconds.

-   **Input**

    Interval


|Parameter name|Port type|Data type|Description|Mandatory?|
|--------------|---------|---------|-----------|----------|
|Interval|Data In|Integer|Timer interval in milliseconds.|Yes|

## Stop method

Stops the timer.

## OnTimeTick event

The event starts when the Start method starts.

|Parameter name|Port type|Data type|Description|Mandatory?|
|--------------|---------|---------|-----------|----------|
|SignalTime|Data Out|Integer|The system date and time when the trigger starts operating.|Yes|
|ElapsedTime|Data Out|Integer|Total time in the timer elapsed.|Yes|

**Parent Topic:**[Timer](../concept/timer.md)

