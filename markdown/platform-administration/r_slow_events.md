---
title: Slow events log record detail
description: As an administrator, you can use Slow Events logs to gain insight into how events are affecting platform performance. To aid in debugging, you can filter slow event log detail by application scope, limiting events to only those events originating in specific scopes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stats Tools, System Diagnostics, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Slow events log record detail

As an administrator, you can use Slow Events logs to gain insight into how events are affecting platform performance. To aid in debugging, you can filter slow event log detail by application scope, limiting events to only those events originating in specific scopes.

<table id="simpletable_uy5_zlw_yp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event name

</td><td>

Name of the event for this record.

</td></tr><tr><td>

Queue

</td><td>

Event queue containing this event.

</td></tr><tr><td>

Event application

</td><td>

Application scope the slow event originated in. Global appears if the slow event originated in the global scope.

</td></tr><tr><td>

Execution count

</td><td>

Number of similar occurrences that are aggregated.

</td></tr><tr><td>

Average execution time \(ms\)

</td><td>

Average duration to execute the event in a single occurrence, in milliseconds.

</td></tr><tr><td>

Day moving average \(ms\)

</td><td>

Average of the moving average values of execution time, calculated over periods of one day.

</td></tr><tr><td>

Last sighting

</td><td>

Time and date the last occurrence was noted.

</td></tr><tr><td>

First sighting

</td><td>

Time and date the first occurrence was noted.

</td></tr><tr><td>

Hash

</td><td>

Hash value for this record.

</td></tr><tr><td>

Month moving average \(ms\)

</td><td>

Average of the moving average values of execution time, calculated over periods of one month.

</td></tr><tr><td>

Label

</td><td>

Label for the event.

</td></tr><tr><td>

Example URL

</td><td>

URL for an individual event.

</td></tr><tr><td>

Example stack trace

</td><td>

Example stack trace for an individual event.

</td></tr><tr><td>

Total execution time

</td><td>

Total sum of the event execution times for the aggregated occurrences.

</td></tr><tr><td>

Event Execution Time / Event Count Trend graphs

</td><td>

Event Execution Time Trend graphs show the total execution time of these events over the most recent period of two hours, one day, or one month. Event Count Trend graphs show the event counts over the most recent period of two hours, one day, or one month.

</td></tr></tbody>
</table>