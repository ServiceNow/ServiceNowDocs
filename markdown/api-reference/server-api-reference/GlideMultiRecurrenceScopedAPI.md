---
title: GlideMultiRecurrence - Scoped
description: The GlideMultiRecurrence API provides methods that return GlideDateTime objects that describe the run times for a specified scheduled job.Returns a GlideDateTime object for each scheduled run time \(occurrence\) that a specified scheduled job should execute within a specific time period, based on the triggers defined in the associated schedule record \(GlideRecord\).
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideMultiRecurrence- Scoped

The GlideMultiRecurrence API provides methods that return GlideDateTime objects that describe the run times for a specified scheduled job.

Use this API when you need to determine when a specific periodic or recurring job needs to run, also known as an occurrence.

This API runs in the `sn_schdl_ns` namespace.

To use this API, the associated scheduling table must contain one or more of the following fields \(triggers\).

<table><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

effective\_end

</td><td>

Scheduled end date and time of the job.

</td></tr><tr><td>

effective\_start

</td><td>

Schedule start date and time of the job.

</td></tr><tr><td>

frequency

</td><td>

Number of occurrences to return.

</td></tr><tr><td>

run\_dayofmonth

</td><td>

Day of the month to run the job. Valid values: 1-31

</td></tr><tr><td>

run\_dayofweek

</td><td>

Day of the week to run the job. Valid values: 1 \(Sunday\) - 7 \(Saturday\)

</td></tr><tr><td>

run\_month

</td><td>

Month of the year to run the job. Valid values: 1-12

</td></tr><tr><td>

run\_time

</td><td>

GMT time of day to run the job.

</td></tr><tr><td>

run\_weekinmonth

</td><td>

Week of month to run the job. Valid values: 1-6

</td></tr><tr><td>

time\_zone

</td><td>

Time zone of the scheduled job.

</td></tr><tr><td>

trigger\_type

</td><td>

-   0: Run once
-   1: Repeat
-   2: On demand
-   3: Day in week
-   4: Day in month
-   5: Week in month
-   6: Day and month in year
-   7: Day in week in month and in year
-   8: Run at the specified times
-   9: Run at system start up
-   10: Interval
-   11: Daily

</td></tr></tbody>
</table>When using this API, you must first create a GlideRecord object for the scheduling table on which the API should act. You then retrieve the scheduling record for which to obtain the occurrence records. For example:

```
var table_nameGR = new GlideRecord('<table_name>'); // Scheduling table, such as sys_trigger
table_nameGR.addQuery('sys_id', '<sys_id>'); // Sys_id of the scheduling record
table_nameGR.query();
table_nameGR.next();  // Retrieve the scheduling record
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideMultiRecurrence - getOccurrences\(\)

Returns a GlideDateTime object for each scheduled run time \(occurrence\) that a specified scheduled job should execute within a specific time period, based on the triggers defined in the associated schedule record \(GlideRecord\).

This method analyzes the current GlideRecord scheduling object, using the triggers defined within the scheduling object, to determine when the job should run.

Properties that control the return results:

-   com.glide.schedule.recurrence.num\_occurrences\_max: Maximum number of occurrences to return.
-   com.glide.schedule.recurrence.num\_occurrences\_default: Default number of occurrences to return.

The method applies the following rules to determine the occurrences to return for the defined period of time and associated triggers:

-   If the **effective\_start** field is valid and not null or empty, use it as the date to start returning occurrences. Otherwise use the current date.
-   If the **effective\_end** date field is valid and not null or empty, return the occurrences between the **effective\_start** and the **effective\_end** date fields.

    Exception to the above rule: If the **effective\_end** date is too far in the future, resulting in the return of more than the number of occurrences specified in the com.glide.schedule.recurrence.num\_occurrences\_max property, then the result is limited to the value specified in com.glide.schedule.recurrence.num\_occurrences\_max \(default 500\).

-   If the **effective\_end** date field is null or empty, but the **frequency** field is set, then use **frequency** to determine the number of occurrences to return.
-   Return historical dates if the **effective\_start** date field is in the past.
-   If the **frequency** and **effective\_end** date fields are both specified, use the **effective\_end** date with the maximum number of occurrences limited to the value specified in the com.glide.schedule.recurrence.num\_occurrences\_max property.

If none of the rules above are true, then the method returns occurrences based on the system properties' default setting.

**Note:** **MAX\_Drift** is not supported by this API.

Example: Both **frequency** and **effective\_end** are specified. **Effective\_end** date takes precedence, and **frequency** is ignored.

-   **frequency**: 10
-   **effective\_start**: 1st Aug 2022
-   **effective\_end**: 10th Oct 2022
-   Trigger type: Day in month
-   Run day of month: 15

Number of GlideDateTime objects returned = 2.

Occurrences returned: 15th Aug 2022, 15th Sep 2022.

Example: Both **frequency** and **effective\_end** are specified. **Effective\_end** date takes precedence and **frequency** is ignored, however, the number of returned occurrences is restricted by the value in the com.glide.schedule.recurrence.num\_occurrences\_max property.

-   **frequency**: 20
-   **effective\_start**: 1st Aug 2022
-   **effective\_end**: 30th Oct 2070
-   Trigger type: Day in month
-   Run day of month: 15

Number of GlideDateTime objects returned = 500.

|Name|Type|Description|
|----|----|-----------|
|grSchedule|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|GlideRecord object pointing to the record containing the job for which you want to get the schedule occurrences.|

|Type|Description|
|----|-----------|
|Array of [GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#) objects|GlideDateTime object for each time that the schedule job should run.|

The following example shows how to retrieve GlideDateTime objects for all scheduled run date/time for a specific period for a specified job schedule record. The selected job is scheduled to run every hour.

```
var sys_id = 'a9e30c7dc61122760116894de7bcc7bd'; // Sys_id of the job schedule record
var table = 'sys_trigger'; // Table that contains the job schedule record

var grSchedule = new GlideRecord(table);
if
 (grSchedule.get(sys_id)) {
  var multiRecurrence = new sn_schdl_ns.GlideMultiRecurrence();
  var dates = multiRecurrence.getOccurrences(grSchedule); // Display the list of occurrences
  for(var i=0; i<dates.length; i++) {
    gs.info('occurrence = ' + dates[i]);
  }
}
```

Output:

```
occurrence = 2022-11-21 16:23:23
occurrence = 2022-11-21 17:23:23
occurrence = 2022-11-21 18:23:23
occurrence = 2022-11-21 19:23:23
occurrence = 2022-11-21 20:23:23
occurrence = 2022-11-21 21:23:23
occurrence = 2022-11-21 22:23:23
occurrence = 2022-11-21 23:23:23
occurrence = 2022-11-22 00:23:23
occurrence = 2022-11-22 01:23:23
```

