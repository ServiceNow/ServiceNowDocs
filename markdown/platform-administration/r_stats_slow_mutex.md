---
title: Slow mutex locks record detail
description: Administrators can use slow mutex logs to gain insight into how mutex locks are affecting platform performance.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Stats Tools, System Diagnostics, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Slow mutex locks record detail

Administrators can use slow mutex logs to gain insight into how mutex locks are affecting platform performance.

<table id="simpletable_uy5_zlw_yp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mutex name

</td><td>

The name of the mutex lock for this record.

</td></tr><tr><td>

Is Fast Lock

</td><td>

If **false**, the lock was placed on a record in the ServiceNow platform. If **true**, the lock was placed on a record in the underlying database.

</td></tr><tr><td>

Average execution time

</td><td>

The average time for which the mutex lock was held.

</td></tr><tr><td>

2-hour moving average \(ms\)

</td><td>

The average of the moving average values of execution time, calculated over periods of two hours.

</td></tr><tr><td>

Day moving average \(ms\)

</td><td>

The average of the moving average values of execution time, calculated over periods of one day.

</td></tr><tr><td>

Month moving average \(ms\)

</td><td>

The average of the moving average values of execution time, calculated over periods of one month.

</td></tr><tr><td>

Execution count

</td><td>

The number of similar occurrences that are aggregated.

</td></tr><tr><td>

Last sighting

</td><td>

The time and date the last occurrence was noted.

</td></tr><tr><td>

First sighting

</td><td>

The time and date the first occurrence was noted.

</td></tr><tr><td>

Example stack trace

</td><td>

A stack trace for an individual mutex lock.

</td></tr><tr><td>

Total execution time

</td><td>

The sum of execution time for the aggregated occurrences.

</td></tr><tr><td>

Has

</td><td>

The hash value for this record.

</td></tr><tr><td>

Label

</td><td>

The mutex lock label.

</td></tr><tr><td>

Example URL

</td><td>

The URL for an individual mutex lock.

</td></tr><tr><td>

Event Execution Time / Event Count Trend graphs

</td><td>

The Mutex Execution Time Trend graphs show the total execution time of these mutex locks over the most recent period of two hours, one day, or one month. The Mutex Count Trend graphs show the mutex lock counts over the most recent period of two hours, one day, or one month.

</td></tr></tbody>
</table>