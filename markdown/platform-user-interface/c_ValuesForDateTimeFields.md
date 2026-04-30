---
title: Values for date/time fields
description: When you filter on fields of type date/time, such as the Created field on any task record, several time-related options are available, such as Today, This week, Last 3 months, and so on.You can filter date and time fields using the operators and values listed here.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Condition builder, Create a condition statement using the condition builder, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Values for date/time fields

When you filter on fields of type date/time, such as the **Created** field on any task record, several time-related options are available, such as **Today**, **This week**, **Last 3 months**, and so on.

For example, at 12:00 on June 1, a user in New York filters a list of incidents using the **Created on Today** condition. The resulting list shows all incidents created during the last twelve hours: between midnight \(00:00:00\) and the user's current time, noon \(12:00:00\), on June 1. A filter for **This week** returns incidents created between the previous Monday at midnight to the current day and time.

A filter for **Last 3 months** returns incidents between midnight on the first of the month three full months ago and the current day and time. For example, if you choose the **Last 3 months** filter on April 15, the results show records created since January 1 up until April 15. A filter for **Last 12 months** returns results from January to January.

A filter for **Last week** returns incidents from midnight on Sunday the week previous ending the following Sunday at midnight. It does not include up to the present day. For example, if you choose the **Last week** filter on Thursday August 17, the results show records created Sunday August 6 up until Sunday August 13.

For the **at or before** and **at or after** filters, use midnight as a start or end point. For example, if you filter a list of incidents created **\[at or after\] \[Yesterday\]**, the resulting list shows all incidents created at midnight yesterday or later. If it is Thursday, August 7, and you filter a list of incidents created **\[at or before\] \[Last week\]**, the resulting list shows all incidents created at and before midnight on Sunday August 3, which is the end of last week.

**Parent Topic:**[Condition builder](c_ConditionBuilder.md)

**Related topics**  


[Filtering on empty fields](../task/t_FilteringOnEmptyFields.md)

[Comparing field values](../../../administer/navigation-and-ui/reference/r_ComparingFieldValues.md)

## Operators and values available for date and time fields

You can filter date and time fields using the operators and values listed here.

|Operator|Definition|Example|
|--------|----------|-------|
|after|Returns records after the specified time period.|A filter run **\[after\] \[Next Month\]** on April 18, 2018 will return records from June 1 and later.|
|at or after|Returns records during and after the specified time period.|A filter run **\[at or after\] \[Next Month\]** on April 18, 2018 will return records from May 1 and later.|
|at or before|Returns records during and before the specified time period.|A filter run **\[at or before\] \[Next Month\]** on April 18, 2018 will return records from May 31 and earlier.|
|before|Returns records before the specified time period.|A filter run **\[before\] \[Next Month\]** on April 18, 2018 will return records from before May 1.|
|between|Returns records between to specified dates.|A filter run **\[between\]** April 18, 2018 \(00:00:00\) and April 19, 2018 \(23:59:59\) will return records on or between the two dates.|
|is anything|Returns all records, including records with empty values in the specified field.|A list of incident records filtered on **\[Created\] \[is anything\]** returns all incidents.|
|is different|Returns records within a different time frame from another field.|A list of incident records filtered on **\[Created\] \[is different\] \[year\] from \[Closed\]** returns records where the values in the **\[Created\]** and **\[Closed\]** field are in different years.|
|is empty|Returns records where the specified field has no value.|A list of incident records filtered on Closed **\[is empty\]** returns records where the Closed field has no value.|
|is less than|Returns records where a field is within specified time frame when compared to another field.|A list of incident records filtered on **\[Closed\] \[is less than\] \[2\] \[hours\] \[after\] \[Created\]** will return results where the **\[Closed\]** value is less than 2 hours after the **\[Created\]** value.|
|is more than|Returns records where a field is beyond the specified time frame when compared to another field.|A list of incident records filtered on **\[Closed\] \[is more than\] \[2\] \[hours\] \[after\] \[Created\]** will return results where the **\[Closed\]** value is more than 2 hours after the **\[Created\]**value.|
|is not empty|Returns records where the specified field has a value.|A list of incident records filtered on **\[Closed\] \[is not empty\]** returns results where the Closed field has a value.|
|is same|Returns records where the two fields share a specified time frame.|A list of incidents filtered on **\[Created\] \[is same\] \[hour\] as \[Closed\]** returns records where the record **\[Created\]** and **\[Closed\]** fields are within the same hour.|
|not on|Returns records that do not match the specified value.|A filter of **\[not on\] \[Today\]** returns records that do not match the current date.|
|on|Returns records on the specified value.|A filter run **\[on\] \[Today\]** on April 18, 2018 will return records from April 18.|
|relative|Returns records with a specified time frame before or after the current time.|A filter run on **\[Created\] \[relative\] \[before\] \[5\] \[minutes\] \[ago\]** run at 12:00:00 returns records from before 11:55:00 of the same date.|
|trend|Returns records on, after and/or before a specified hour of the day, day of the week, week of the year, month, quarter, or year.|A filter of **\[Created\] \[trend\] \[Monday\]** returns records where the **\[Created\]** date falls on a Monday.|

<table id="table_aqk_yqz_fdb"><thead><tr><th>

Value

</th><th>

Definition

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Current hour/minute

</td><td>

Returns records matching the current hour or minute

</td><td>

A filter run **\[on\] \[Current hour\]** on April 18 \(12:02:00\), would return records from April 18 \(12:00:00\) to April 18 \(12:59:59\)

</td></tr><tr><td>

Last **n** minutes/hours/days/weeks/months/quarters/years

</td><td>

Returns records within the previous selected time period, starting with the beginning of that time frame.

</td><td>

A filter run **\[on\] \[Last 3 months\]** on April 18, would return records from January 1 up until April 18.**Note:** Years returns results from January to January.

</td></tr><tr><td>

Next **n** weeks/months/quarters/years

</td><td>

Returns records within the next selected time period, including records with values up to the end of that time frame.

</td><td>

A filter run **\[on\] \[Next year\]** on April 18, 2018 will return any records with a date in 2019, including dates in 2019 after April 18.

</td></tr><tr><td>

One year ago

</td><td>

Returns records from the current time, one year ago to the end of the current month

</td><td>

A filter run **\[on\] \[One year ago\]** on April 18, 2018 \(12:00:00\) will return records from April 18, 2017 \(12:00:00\) to April 30 \(23:59:59\)

</td></tr><tr><td>

This week/month/quarter/year

</td><td>

Returns records with the current selected time period.

</td><td>

A filter run **\[on\] \[This week\]** on April 18, 2018 will return records from April 15 \(00:00:00\) to April 21 \(23:59:59\)

</td></tr><tr><td>

Today

</td><td>

Returns records between midnight of the current day and midnight of the next day

</td><td>

A filter run **\[on\] \[Today\]** on April 18, 2018 will return records from April 18 \(00:00:00\) to April 18 \(23:59:59\)

</td></tr><tr><td>

Tomorrow

</td><td>

Returns records between midnight \(00:00:00\) and the current time.

</td><td>

A filter run **\[on\] \[Tomorrow\]** on April 18, 2018 will return records from April 19 \(00:00:00\) to April 19 \(23:59:59\)

</td></tr><tr><td>

Yesterday

</td><td>

Returns records between midnight of the previous day and midnight of the current day.

</td><td>

A filter run **\[on\] \[Yesterday\]** on April 18, 2018 will return records from April 17 \(00:00:00\) to April 17 \(23:59:59\)

</td></tr></tbody>
</table>