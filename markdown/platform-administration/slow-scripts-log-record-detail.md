---
title: Slow scripts log record detail
description: As an administrator, you can use Slow Scripts logs to gain insight into how events are affecting platform performance. To aid in debugging, you can filter a slow script log by application scope, limiting scripts to only those scripts originating in specific scopes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Stats Tools, System Diagnostics, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Slow scripts log record detail

As an administrator, you can use Slow Scripts logs to gain insight into how events are affecting platform performance. To aid in debugging, you can filter a slow script log by application scope, limiting scripts to only those scripts originating in specific scopes.

<table id="simpletable_uy5_zlw_yp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label assigned to the script.

</td></tr><tr><td>

Script source

</td><td>

Source of the script.

</td></tr><tr><td>

Script application

</td><td>

Application scope the slow script originated in. Global appears if the script originated in the global scope.

</td></tr><tr><td>

Average execution time \(ms\)

</td><td>

Average duration to execute the script in a single occurrence, in milliseconds.

</td></tr><tr><td>

Execution count

</td><td>

Number of similar occurrences that are aggregated.

</td></tr><tr><td>

Day moving average \(ms\)

</td><td>

Average of the moving average values of execution time, calculated over periods of one day.

</td></tr><tr><td>

Original application

</td><td>

Total sum of the script execution times for the aggregated occurrences.

</td></tr><tr><td>

Last sighting

</td><td>

Time and date at which the script was last executed.

</td></tr></tbody>
</table>