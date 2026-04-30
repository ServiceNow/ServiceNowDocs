---
title: Date and time transform functions
description: Use date and time transform functions to recalculate or reformat data pills for Date/Time values.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Transform functions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Date and time transform functions

Use date and time transform functions to recalculate or reformat data pills for Date/Time values.

Date and time transform functions require a Date/Time or String input data pill. Some functions also support Duration data pills. Make sure to use the correct input [data pill type](action-inputs-outputs.md) when applying date and time transform functions. If a date and time transform function is applied to an improper data pill type, the data is not transformed at runtime and the input value is returned instead. For more information on confirming your flow runtime values, see [Test a flow](../task/flow-test.md).

**Note:** Runtime Date/Time values are not localized and appear in the UTC \(Coordinated Universal Time\) time zone. For more information, see [Time zones](https://www.servicenow.com/docs/access?context=r_TimeZones&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and [time zone representation](https://support.servicenow.com/kb_view.do?sysparm_article=KB0594661).

## Add Time

Adds days, hours, minutes, or seconds to an input Date/Time, Date, Due Date, or Duration.

<table id="table_elj_cdf_mkb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

Date/Time, Date, Due Date, or Duration**Note:** If the input is a Date or Due Date, the transform creates a full Date/Time value using time values of hour 0, minute 0, and second 0.

</td><td>

**Duration** - Amount of time to add in days, hours, minutes, and seconds

</td><td>

Date/Time - Transformed Date/Time value after adding the specified **Duration**

</td></tr></tbody>
</table>-   Input: `2019-09-12 11:00:00`
-   Duration: `3 hours`
-   Output: `2019-09-12 14:00:00`

## Subtract Time

Subtracts days, hours, minutes, and/or seconds from the input Date/Time, Date, Due Date, or Duration.

<table id="table_lvd_jff_mkb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

Date/Time, Date, Due Date, or Duration**Note:** If the input is a Date or Due Date, the transform creates a full Date/Time value using time values of hour 0, minute 0, and second 0.

</td><td>

**Duration** - Enter an amount of time to subtract in days, hours, minutes, and seconds

</td><td>

Date/Time - Transformed Date/Time value after subtracting the specified **Duration**

</td></tr></tbody>
</table>-   Input: `2019-09-12 11:00:00`
-   Duration: `2 days, 1 hours, 5 minutes, 10 seconds`
-   Output: `2019-09-10 09:54:50`

In this example, the flow retrieves a CMDB Configuration Item record from a remote instance. The Subtract Time transform function then localizes the value of the **Created** field by subtracting three hours from the input Date/Time.

![Localize a field value's time zone.](../images/subtract-time-transform-function-example.png "Localize a field value's time zone")

## String to Date

Converts the input String to a Date/Time.

<table id="table_crn_5ff_mkb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

String formatted as specified in the **Input Date Format**

</td><td>

-   **Input Date Format** - Date/Time or date format of the input String
-   **Custom Format** - Valid Date/Time or date format represented as a String. Required only if Custom Format is selected as the **Input Date Format**.

</td><td>

Date/Time

</td></tr></tbody>
</table>**Note:**

-   If the Date/Time value for the **Custom Format** input is incomplete, the transform creates a full Date/Time value using default dates and times. In such a case, the transform defaults to the current year, the current month, day 1 of a month, hour 0, minute 0, and second 0. For example, an input data pill value of **Oct 2019** and a custom date format of **MMM yyyy** produces an output of `2019-10-01 00:00:00`.
-   If you use an incorrect data pill type or invalid **Custom Format**, the flow cancels during runtime.

-   Input: `'1995-11-20'`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output: `1995-11-20 00:00:00`

## Date to String

Converts the input Date/Time, Date, or Due Date to a String. Select a **Date Format** for the input Date/Time. Alternatively, enter a **Custom Format** for the input Date/Time.

<table id="table_pxn_5gf_mkb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

Date/Time, Date, or Due Date

</td><td>

-   **Output Date Format** - Date/Time or date format of the output String
-   **Custom Format** - Valid Date/Time or date format represented as a String. Required only if selecting Custom Format as the **Date Format**.

</td><td>

String formatted as specified in the **Output Date Format**

</td></tr></tbody>
</table>**Note:** If you use an incorrect input data pill type or invalid **Custom Format**, the flow cancels during runtime.

-   Input: `1969-12-31 14:23:57`
-   Output Date Format: `Custom (enter below)`
-   Custom Format: `'On' MMM dd, yyyy 'at' hh:mm a`
-   Output: `'On Dec 31, 1969 at 2:23 PM'`

In this example, the flow retrieves a User \[sys\_user\] record from a third-party database. The Date to String transform function converts the format of the **Created** field and then logs the date, time, and name that is associated with the record.

![Concatenate a Date/Time value with a String value.](../images/date-to-string-transform-function-example.png "Concatenate a Date/Time value with a String value")

## Custom date formats

You can specify a custom date format with a sequence of specific date and time pattern strings. A pattern string consists of one or more uppercase and lowercase letters from A to Z. Any text within quotation marks is ignored and is instead copied into the date output.

|String|Description|Output Format|Example|
|------|-----------|-------------|-------|
|G|Era designator|Text|AD|
|y|Year|Year|2019; 19|
|Y|Week in year|Year|2019; 19|
|M|Month in year \(within date\)|Month|July; Jul; 07|
|L|Month in year \(standalone value\)|Month|July; Jul; 07|
|w|Week in year|Number|52|
|W|Week in month|Number|1|
|D|Day in year|Number|365|
|d|Day in month|Number|2|
|F|Day of week in month|Number|3|
|E|Day name in week|Text|Wednesday; Wed|
|u|Day number of week|Number|3|
|a|a.m. or p.m.|Text|p.m.|
|H|Hour in day from 0 through 23|Number|0|
|k|Hour in day from 1 through 24|Number|24|
|K|Hour in a.m. or p.m. from 0 through 11|Number|0|
|h|Hour in a.m. or p.m. from 1 through 12|Number|12|
|m|Minute in hour|Number|59|
|s|Second in minute|Number|1|
|S|Millisecond|Number|500|
|z|Time zone in default format|Time zone in default format|Pacific Standard Time; PST|
|Z|Time zone in RFC 822 format|Time zone in RFC 822 format|-0800|
|X|Time zone in ISO 8601 format|Time zone in ISO 8601 format|-08; -0800; -08:00|

## Day

Retrieves the day component from the specified Date/Time.

|Input data pill|Output data pill|
|---------------|----------------|
|Date/Time|Integer - Day from the specified date.|



-   Input: `2021-11-20 13:06:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output: `20`

## Hour

Retrieves the hour component from the specified Date/Time.

|Input data pill|Output data pill|
|---------------|----------------|
|Date/Time|Integer - Hour from the specified date.|

-   Input: `2021-11-20 13:06:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output:`13`

## Minute

Retrieves the minute component from the specified Date/Time.

|Input data pill|Output data pill|
|---------------|----------------|
|Date/Time|Integer - Minute component from the specified date.|

-   Input: `2021-11-20 13:06:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output: `06`

## Second

Retrieves the second component from the specified Date/Time.

|Input data pill|Output data pill|
|---------------|----------------|
|Date/Time|Integer - Second component from the specified date.|

-   Input: `2021-11-20 13:06:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output: `12`

## Month

Retrieves the month component from the specified Date/Time.

|Input data pill|Output data pill|
|---------------|----------------|
|Date/Time|Integer - Month component from the specified date.|

-   Input: `2021-11-20 13:06:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output: `11`

## Week

Evaluates the week number for the specified Date/Time.

|Input data pill|Output data pill|
|---------------|----------------|
|Date/Time|Integer - Week number for the specified date.|

-   Input: `2021-04-07 12:01:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output: `15`

## Year

Retrieves the year component from the specified Date/Time.

|Input data pill|Output data pill|
|---------------|----------------|
|Date/Time|Integer - Year component from the specified date.|

-   Input: `2021-04-07 12:01:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Output: `2021`

## Date Difference

Evaluates the time duration difference between the specified input date and the parameter date and then adds the difference time duration to the Epoch time \(1970-01-01 00:00:00\).

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Date/Time, Date, or Due Date|Date/Time, Date, or Due Date|Duration - Time duration difference added to the Epoch time \(1970-01-01 00:00:00\).|

-   Input: `2021-05-02 09:10:12`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Parameters: `2021-04-07 06:02:23`
-   Output: `1970-01-26 03:07:49`

## End of Month

Evaluates the last day of the month after adding the specified number of the months to the specified date.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Date|Number of Months - Months to add to the specified date.|Integer - Last day of the month after adding the number of months to the specified input date.|

-   Input: `2021-11-20`
-   Input Date Format: `ISO Date (2004-06-28)`
-   Number of Months: `3`
-   Output: `2022-02-28`

**Parent Topic:**[Transform functions](../concept/transform-functions.md)

