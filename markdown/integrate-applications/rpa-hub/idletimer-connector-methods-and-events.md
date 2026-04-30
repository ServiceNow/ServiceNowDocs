---
title: IdleTimer connector methods and events
description: Learn about the IdleTimer connector methods and events.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IdleTimer connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# IdleTimer connector methods and events

Learn about the IdleTimer connector methods and events.

## Start method

Sets the maximum idle time in seconds.

|Parameter name|Port type|Data type|Description|Mandatory?|
|--------------|---------|---------|-----------|----------|
|MaxIdleTime|Data In|Integer|Maximum idle time in seconds.|Yes|

## Stop method

Stops the timer.

## OnIdleStart

Triggers the automation when the Start method is executed.

## OnIdleStop

Stops the automation when the Start method is executed.

**Parent Topic:**[IdleTimer connector](../concept/idletimer-connector.md)

