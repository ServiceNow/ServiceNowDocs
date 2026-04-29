---
title: System Events
description: Events are special records that the system uses to log when certain conditions occur and to take some kind of action in response to the conditions.
locale: en-US
release: australia
product: System Events
classification: system-events
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring system events, System Events, Configure core features, Administer the ServiceNow AI Platform]
---

# System Events

Events are special records that the system uses to log when certain conditions occur and to take some kind of action in response to the conditions.

The system uses business rules to monitor for system conditions and to generate event records in the Event \[sysevent\] table, which is also known as the event log or event queue.

Event-generating business rules typically use this script logic:

If \[some condition is true for the current record\], then \[add a specific event to the queue\].

For example, here are some of the conditions in the **incident event** business rule:

-   If a user adds a comment to an incident record, add an **incident.commented** event.
-   If a user adds an incident record, add an **incident.inserted** event.
-   If a user updates an incident record, add an **incident.updated** event.

Event-generating business rules use the GlideSystem eventQueue method to insert event records, which typically contain this information:

|Field|Description|
|-----|-----------|
|Name|Unique name of event. Baseline event names include the record affected and the triggering action, such as **incident.commented**.|
|Parm1|Event-specific parameter the system uses to pass record information to other parts of the system, such as a record Sys ID or a field value.|
|Parm2|Event-specific parameter the system uses to pass record information to other parts of the system, such as a record Sys ID or a field value.|
|Table|Table to which the event applies. This is the same table on which the business rule ran.|
|Instance|Sys ID of the record to which this event applies.|

Scheduled jobs periodically read the event queue and forward them to the appropriate handler for processing. The handler uses information from event records to take some kind of action such as:

-   Run a script action
-   Send a notification
-   Trigger a workflow activity
-   Trigger an inactivity monitor

By default, the system provides events covering a broad view of application activity. If existing events do not meet your needs, you can create your own events to watch for specific changes to records.

For developer training, see [Scheduled Script Executions and Events Objectives](https://developer.servicenow.com/dev.do#!/learn/courses/xanadu/app_store_learnv2_automatingapps_xanadu_automating_application_logic/app_store_learnv2_automatingapps_xanadu_scheduled_script_executions_and_events/app_store_learnv2_automatingapps_xanadu_scheduled_script_executions_and_events_objectives) on the ServiceNow® Developer Site.

Use the [System Events and Jobs Dashboard](track-events.md) to monitor the system event processing system and the scheduled jobs processing system.

## Event processing during platform upgrade

Determine which events are to be processed during a platform upgrade by configuring the following properties:

-   **glide.event\_processor.all\_events\_upgrade\_safe**: Set to **true** to process all events during platform upgrade. Default = **false**.
-   **glide.event\_processor.upgrade\_safe\_events**: Configure a comma-separated list of event names to indicate that only specified events are processed. Default = &lt;empty&gt;.

    This property is relevant only when **glide.event\_processor.all\_events\_upgrade\_safe = false**.


