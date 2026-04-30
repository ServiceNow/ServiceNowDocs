---
title: View event processing statistics
description: Extract statistics from your instance to ensure that performance is not affected and extract metrics related to event processes to monitor event processing status.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# View event processing statistics

Extract statistics from your instance to ensure that performance is not affected and extract metrics related to event processes to monitor event processing status.

## Before you begin

Ensure that the **Event Management - Collect xmlstats** job is active. Configure this scheduled job by navigating to **System Definition** &gt; **Scheduled Jobs**.

You can control the processing of event statistics using the **evt\_mgmt.event\_processing\_stats\_period** property. For information about configuring this property, see [Configure statistics processing period](add-property-statistics-processing-period.md).

Role required: evt\_mgmt\_operator

## About this task

You can view key metrics from the instance to ensure that performance is not affected and monitor the status of the processing of events. For more information about viewing self-health monitoring statistics, see [View self-health monitoring statistics for Metric Intelligence](xmlstats-oi-self-health.md).

## Procedure

1.  In a browser where the instance is running, run the XML Stats script by appending the following text to the instance URL: `xmlstats.do?include=XMLStatsEm`

2.  Press **Enter**.

3.  Monitor the event processing metrics that are reported to ensure that events are processed according to accepted benchmark values.


## Result

## Sample output after running the XML Stats script

```
<xmlstats created="Tue Oct 23 04:01:25 PDT 2018" includes="XMLStatsEm" version="2">
<itom_event_management>
<event_processing>
<processed count="47" max_process_time="10" mean_process_time="5" record_time="2018-10-23 11:00:41"/>
<ready count="7" oldest_ready_event="37" record_time="2018-10-23 11:00:41"/>
<error count="5" record_time="2018-10-23 11:00:41"/>
<total_created count="5" record_time="2018-10-23 11:00:41"/>
</event_processing>
</itom_event_management>
</xmlstats>
```

The event processing metrics in the report are described in the following table.

**Note:** The default processing cycle is events created in the last hour and updated in the last minute.

<table id="table_vtl_5kd_wfb"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Event processing statistics

</td></tr><tr><td>

processed count=n

</td><td>

Number of events processed by the instance.

</td></tr><tr><td>

max\_process\_time=n

</td><td>

Longest time taken by the instance to process an event.

</td></tr><tr><td>

mean\_process\_time=n

</td><td>

Average time taken by the instance to process the events in this cycle.

</td></tr><tr><td class="sub-head" colspan="2">

Event ready statistics

</td></tr><tr><td>

ready count=n

</td><td>

Number of events that are in Ready state and are available to be processed.Default processing cycle: events created in the last hour and updated in the last minute.

</td></tr><tr><td>

oldest\_ready\_event=n

</td><td>

Longest time taken by an event to remain in Ready state. If this metric has a value that is bigger than your benchmark figure, investigate the event further to determine what is impeding the processing.Default processing cycle: events created in the last hour.

</td></tr><tr><td class="sub-head" colspan="2">

Other processing statistics

</td></tr><tr><td>

error count=n

</td><td>

Number of events for which errors were reported.Default processing cycle: events created in the last hour and updated in the last minute.

</td></tr><tr><td>

total\_created count=n

</td><td>

Overall number of events that were processed during this event processing cycle.Default processing cycle: events created in the last hour.

</td></tr></tbody>
</table>-   **[Enable processing of event process statistics](add-property-enabling-statistics-processing.md)**  
Enable the system property that switches on statistics processing for events to let the platform collect and analyze metrics such as event volume, processing flow, and handling time. This helps you monitor system performance, identify bottlenecks, and optimize event handling for faster and more efficient operations.
-   **[Configure statistics processing period](add-property-statistics-processing-period.md)**  
Set the time period, in seconds, for collecting event processing statistics. For example, you can set a time period twice as long as the default 60 seconds to collect more statistics.

**Parent Topic:**[Processing Events](../concept/processing-events.md)

