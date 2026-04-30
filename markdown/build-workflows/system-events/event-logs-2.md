---
title: Event logs
description: The event log records all system events that occur within the ServiceNow AI Platform.
locale: en-US
release: zurich
product: System Events
classification: system-events
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System events reference, System Events, Build workflows]
---

# Event logs

The event log records all system events that occur within the ServiceNow AI Platform.

This log provides the following information for all events that occur:

|Field|Description|
|-----|-----------|
|Created|Date and time of the event for the locale of the machine running the instance.|
|Name|Name of the event as listed in the Event Registry.|
|URI|HTTP query that generated the event.|
|Parm1|Event-specific value that depends on the event and the recipient.|
|Parm2|Event-specific value that depends on the event and the recipient.|
|Table|Database table acted on for this event.|
|Processed|Date and time the event started processing. This time reflects the locale of the machine running the instance.|
|Processing time|Time taken to process this event, in milliseconds.|
|Queue|Processor queue name.|

**Parent Topic:**[System events reference](system-events-reference.md)

