---
title: MobileGlideDateTime - Scoped
description: The MobileGlideDateTime API provides methods for working with date and time values in mobile scripts. Capabilities include comparing two values, formatting a value for display, reading parts of a value like the month or day of the week, and checking time zone and daylight saving time information.Compares this date and time value with another date and time value and returns a number that indicates whether this value is earlier than, the same as, or later than the other value.Compares this datetime with another MobileGlideDateTime for equality, or determines whether it occurs after, before, on-or-after, or on-or-before the specified datetime. Use these methods when you need a true or false result, such as in a button condition.Gets the date portion of the date and time value as a MobileGlideDate object. Use getDate\(\) for the date in the system time zone, and getLocalDate\(\) for the date in the current user’s time zone.Gets the day of the month, in the user's time zone or in UTC.Gets the day of the week, in the user's time zone or in UTC.Gets the number of days in the month, in the user's time zone or in UTC.Gets the amount of time, in milliseconds, that daylight saving time is offset.Gets the current error message.Gets the month, in the user's time zone or in UTC.Gets the date and time value as the number of milliseconds since January 1, 1970, 00:00:00 GMT. Use this method to compare, sort, or calculate the time between date and time values.Gets the time-of-day portion of this date and time. getTime\(\) returns the time in the system time zone, and getLocalTime\(\) returns it in the current user's time zone.Gets the offset between the time zone and UTC, in milliseconds.Gets the date and time in the current user's time zone. getUserFormattedLocalTime\(\) returns the value in the user's display format, and getInternalFormattedLocalTime\(\) returns it in the internal format.Gets the date-time value. getValue\(\) returns the internal-format value; getDisplayValue\(\) returns the current user's display-format value; getDisplayValueInternal\(\) returns the display value expressed in the internal format.Gets the number of the week in the year. getWeekOfYearLocalTime\(\) returns the week in the user's time zone, and getWeekOfYearUTC\(\) returns the week in UTC.Gets the four-digit year of this date and time. getYearLocalTime\(\) returns the value in the current user's time zone and getYearUTC\(\) returns the value in UTC.Determines whether this datetime uses a daylight saving offset.Determines whether the value is a valid date and time.Gets the date and time value as a string in the internal format, yyyy-MM-dd HH:mm:ss, such as for adding the value to a log message.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileGlideDateTimeScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 22
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideDateTime - Scoped

The MobileGlideDateTime API provides methods for working with date and time values in mobile scripts. Capabilities include comparing two values, formatting a value for display, reading parts of a value like the month or day of the week, and checking time zone and daylight saving time information.

MobileGlideDateTime provides the subset of GlideDateTime that can be evaluated against the local database on a device. It gives a script structured access to the components of a date and time value, including the day, month, year, and week, in both local time and UTC, as well as comparison operators. A value can also be split into a[MobileGlideDate - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md) and [MobileGlideTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md) pair.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

For guidance on date time input strings with a list of common format conflicts, refer to [Server-side script use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/useful-server-side-scripts.md).

This API contains the following capabilities:

-   Comparing date and time values: [MobileGlideDateTime - compareTo\(MobileGlideDateTime gdt\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - equals\(\) / after\(\) / before\(\) / onOrAfter\(\) / onOrBefore\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)
-   Getting the value as a string or number: [MobileGlideDateTime - getValue\(\) / getDisplayValue\(\) / getDisplayValueInternal\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getUserFormattedLocalTime\(\) / getInternalFormattedLocalTime\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - toString\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getNumericValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)
-   Splitting the value into a date or time: [MobileGlideDateTime - getDate\(\) / getLocalDate\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getTime\(\) / getLocalTime\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)
-   Getting parts of the value: [MobileGlideDateTime - getYearLocalTime\(\) / getYearUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getMonthLocalTime\(\) / getMonthUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getWeekOfYearLocalTime\(\) / getWeekOfYearUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getDayOfMonthLocalTime\(\) / getDayOfMonthUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getDayOfWeekLocalTime\(\) / getDayOfWeekUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getDaysInMonthLocalTime\(\) / getDaysInMonthUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)
-   Getting time zone and daylight saving time information: [MobileGlideDateTime - getTZOffset\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getDSTOffset\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - isDST\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)
-   Validating the value: [MobileGlideDateTime - isValid\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md), [MobileGlideDateTime - getErrorMsg\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public value constructor. Obtain an instance from the `nowGlideDateTime()` method of [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md).

## MobileGlideDateTime - compareTo\(MobileGlideDateTime gdt\)

Compares this date and time value with another date and time value and returns a number that indicates whether this value is earlier than, the same as, or later than the other value.

|Name|Type|Description|
|----|----|-----------|
|gdt|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)|Date and time value \(gdt\) to compare with this value.|

<table id="table_MGDT-compareTo_M_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number that indicates how this value compares with the specified value.Possible values:

-   `0`: This value is earlier than the specified value.
-   `1`: The values are the same.
-   `-1`: This value is later than the specified value.

Range: -1 to 1

</td></tr></tbody>
</table>This example compares the current date and time with a second value and logs the result. A result of `0` means the two values are equal.

```
mgs.info(mgs.nowGlideDateTime().compareTo(mgs.nowGlideDateTime()));
```

Output:

```
0
```

This example checks a record’s due date and logs whether the record is overdue, due now, or on schedule. The record’s due date is in the future.

```
var now = mgs.nowGlideDateTime();
        var dueDate = current.due_date.getValue();
        var result = now.compareTo(dueDate);
        if (result > 0) {
        mgs.info('Overdue');
        } else if (result === 0) {
        mgs.info('Due now');
        } else {
        mgs.info('On schedule');
        }
```

Output:

```
On schedule
```

## MobileGlideDateTime - equals\(\) / after\(\) / before\(\) / onOrAfter\(\) / onOrBefore\(\)

Compares this datetime with another MobileGlideDateTime for equality, or determines whether it occurs after, before, on-or-after, or on-or-before the specified datetime. Use these methods when you need a true or false result, such as in a button condition.

|Name|Type|Description|
|----|----|-----------|
|gdt|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)|The datetime to compare against.|

<table id="table_MGDT-equals_after_before_onOrAfter_onOrBefore_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

-   equals\(\): Flag that indicates whether this date and time value is the same as the specified value.

Valid values: `true`: The values are equal. `false`: The values aren’t equal.

-   after\(\): Flag that indicates whether this date and time value is later than the specified value.

Valid values: `true`: This value is later. `false`: This value is the same or earlier.

-   before\(\): Flag that indicates whether this date and time value is earlier than the specified value.

Valid values: `true`: This value is earlier. `false`: This value is the same or later.

-   onOrAfter\(\): Flag that indicates whether this date and time value is the same as or later than the specified value.

Valid values: `true`: This value is the same or later. `false`: This value is earlier.

-   onOrBefore\(\): Flag that indicates whether this date and time value is the same as or earlier than the specified value.

Valid values: `true`: This value is the same or earlier. `false`: This value is later.


</td></tr></tbody>
</table>This example checks whether the current date and time is after a record’s due date and logs the result.

```
var dueDate = new MobileGlideDateTime(current.due_date.getValue());
var now = mgs.nowGlideDateTime();
mgs.info(now.after(dueDate));
```

Output:

```
false
```

This example checks whether the current date and time is before a visit’s scheduled start. A button condition can use this check to show a Cancel visit button only until the visit starts. The scheduled start is in the future.

```
var scheduledStart = current.scheduled_start.getValue();
        var now = mgs.nowGlideDateTime();
        var canCancel = now.before(scheduledStart);
        mgs.info('Show Cancel visit button: ' + canCancel);
```

Output:

```
Show Cancel visit button: true
```

This example checks whether a record’s due date is the same as the current date and time and logs the result. The record’s due date is in the future.

```
var now = mgs.nowGlideDateTime();
        var dueDate = current.due_date.getValue();
        mgs.info('Due now: ' + now.equals(dueDate));
```

Output:

```
Due now: false
```

This example checks whether a visit’s scheduled start has been reached. A button condition can use this check to show a Start work button only once the visit starts. The scheduled start is in the past.

```
var now = mgs.nowGlideDateTime();
        var scheduledStart = current.scheduled_start.getValue();
        var canStart = now.onOrAfter(scheduledStart);
        mgs.info('Show Start work button: ' + canStart);
```

Output:

```
Show Start work button: true
```

This example checks whether a time sheet can still be edited. A button condition can use this check to show an Edit time sheet button up to and including the submission deadline. The deadline is in the future.

```
var now = mgs.nowGlideDateTime();
        var deadline = current.submission_deadline.getValue();
        var canEdit = now.onOrBefore(deadline);
        mgs.info('Show Edit time sheet button: ' + canEdit);
```

Output:

```
Show Edit time sheet button: true
```

## MobileGlideDateTime - getDate\(\) / getLocalDate\(\)

Gets the date portion of the date and time value as a MobileGlideDate object. Use getDate\(\) for the date in the system time zone, and getLocalDate\(\) for the date in the current user’s time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideDate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md)|MobileGlideDate object that contains the year, month, and day of the date and time value, with no time of day. For the methods that you can call on this object, see the reference for [MobileGlideDate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md).|

This example gets the date portion of the current date and time in the user’s time zone and logs it in `MM/dd/yyyy` format.

```
var date = mgs.nowGlideDateTime().getLocalDate();
mgs.info(date.getByFormat('MM/dd/yyyy'));
```

Output:

```
"08/26/2026"
```

This example builds a daily report reference from the date in the user’s time zone. Use getLocalDate\(\) when the date should match the user’s calendar day. Use getDate\(\) when the date should match the system time zone.

```
var localDate = mgs.nowGlideDateTime().getLocalDate();
        var reportRef = 'DAILY-' + localDate.getValue();
        mgs.info(reportRef);
```

Output:

```
DAILY-2026-08-26
```

This example gets the date portion of the current date and time in the system time zone and logs it in the internal format, `yyyy-MM-dd`.

```
var date = mgs.nowGlideDateTime().getDate();
        mgs.info(date.getValue());
```

Output:

```
2026-08-26
```

## MobileGlideDateTime - getDayOfMonthLocalTime\(\) / getDayOfMonthUTC\(\)

Gets the day of the month, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getDayOfMonthLocalTime_getDayOfMonthUTC_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Day of the month. Range: 1-31

</td></tr></tbody>
</table>This example gets the current day of the month in the user’s time zone and logs it.

```
mgs.info(mgs.nowGlideDateTime().getDayOfMonthLocalTime());
```

Output:

```
26
```

This example determines which half of the month the current date falls in, such as to label a time entry with its pay period.

```
var day = mgs.nowGlideDateTime().getDayOfMonthLocalTime();
        var payPeriod = day <= 15 ? 'First half' : 'Second half';
        mgs.info('Day ' + day + ': ' + payPeriod + ' pay period');
```

Output:

```
Day 26: Second half pay period
```

This example gets the current day of the month in UTC. A script can use this value to group records into daily totals that are the same for users in every time zone.

```
var day = mgs.nowGlideDateTime().getDayOfMonthUTC();
        mgs.info('Daily total for day ' + day + ' (UTC)');
```

Output:

```
Daily total for day 26 (UTC)
```

## MobileGlideDateTime - getDayOfWeekLocalTime\(\) / getDayOfWeekUTC\(\)

Gets the day of the week, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getDayOfWeekLocalTime_getDayOfWeekUTC_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Day of the week. Range: 1-7 \(Monday = 1\)

</td></tr></tbody>
</table>This example checks whether the current day of the week, in the user’s time zone, is Monday and logs the result.

```
var isMonday = mgs.nowGlideDateTime().getDayOfWeekLocalTime() === 1;
mgs.info(isMonday);
```

Output:

```
false
```

This example checks whether the current day is a weekend day. A button condition can use this check to show a Request weekend coverage button only on Saturdays and Sundays. Monday is 1 and Sunday is 7.

```
var dayOfWeek = mgs.nowGlideDateTime().getDayOfWeekLocalTime();
        var isWeekend = dayOfWeek === 6 || dayOfWeek === 7;
        mgs.info('Day of week: ' + dayOfWeek + ', weekend: ' + isWeekend);
```

Output:

```
Day of week: 3, weekend: false
```

This example checks whether the current day in UTC is Sunday, when a weekly system maintenance runs. Monday is 1 and Sunday is 7.

```
var dayOfWeek = mgs.nowGlideDateTime().getDayOfWeekUTC();
        var isMaintenanceDay = dayOfWeek === 7;
        mgs.info('Day of week: ' + dayOfWeek + ', maintenance day: ' + isMaintenanceDay);
```

Output:

```
Day of week: 3, maintenance day: false
```

## MobileGlideDateTime - getDaysInMonthLocalTime\(\) / getDaysInMonthUTC\(\)

Gets the number of days in the month, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getDaysInMonthLocalTime_getDaysInMonthUTC_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of days in the month. Range: 28-31

</td></tr></tbody>
</table>This example gets the number of days in the current month, in the user’s time zone, and logs it.

```
mgs.info(mgs.nowGlideDateTime().getDaysInMonthLocalTime());
```

Output:

```
31
```

This example calculates how many days are left in the current month, such as to show how much time remains to meet a monthly quota.

```
var gdt = mgs.nowGlideDateTime();
        var daysLeft = gdt.getDaysInMonthLocalTime() - gdt.getDayOfMonthLocalTime();
        mgs.info(daysLeft + ' days left in the month');
```

Output:

```
5 days left in the month
```

This example gets the last day of the current billing month, which is defined in UTC.

```
var lastDay = mgs.nowGlideDateTime().getDaysInMonthUTC();
        mgs.info('Billing period ends on day ' + lastDay + ' (UTC)');
```

Output:

```
Billing period ends on day 31 (UTC)
```

## MobileGlideDateTime - getDSTOffset\(\)

Gets the amount of time, in milliseconds, that daylight saving time is offset.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getDSTOffset_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Amount of time that daylight saving time shifts the clock from standard time.Unit: milliseconds

</td></tr></tbody>
</table>This example gets the daylight saving time offset, in milliseconds, for the current date and time and logs it.

```
mgs.info(mgs.nowGlideDateTime().getDSTOffset());
```

Output:

```
0
```

This example converts the daylight saving time offset from milliseconds to hours so it can be shown in a message.

```
var offsetHours = mgs.nowGlideDateTime().getDSTOffset() / (60 * 60 * 1000);
        mgs.info('Daylight saving adjustment: ' + offsetHours + ' hours');
```

Output:

```
Daylight saving adjustment: 0 hours
```

## MobileGlideDateTime - getErrorMsg\(\)

Gets the current error message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current error message. Returns null if there is no error. The backing field is only ever assigned when a real error occurs, such as an unparseable date/time string. It is never set to an empty string.|

This example logs the current error message. The method returns `null` when there is no error.

```
mgs.info(mgs.nowGlideDateTime().getErrorMsg());
```

Output:

```
null
```

This example checks for an error message before the script uses the date and time value.

```
var gdt = mgs.nowGlideDateTime();
        var error = gdt.getErrorMsg();
        if (error) {
        mgs.info('Date error: ' + error);
        } else {
        mgs.info('Date value is valid.');
        }
```

Output:

```
Date value is valid.
```

## MobileGlideDateTime - getMonthLocalTime\(\) / getMonthUTC\(\)

Gets the month, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getMonthLocalTime_getMonthUTC_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Month of the date and time value, where 1 is January and 12 is December.Range: 1-12

</td></tr></tbody>
</table>This example gets the current month number, in the user’s time zone, and logs it.

```
mgs.info(mgs.nowGlideDateTime().getMonthLocalTime());
```

Output:

```
8
```

This example converts the current month number to a month name, such as to label a monthly report.

```
var months = ['January', 'February', 'March', 'April', 'May', 'June',
        'July', 'August', 'September', 'October', 'November', 'December'];
        var month = mgs.nowGlideDateTime().getMonthLocalTime();
        mgs.info('Report for ' + months[month - 1]);
```

Output:

```
Report for August
```

This example builds a year-month key, such as 2026-08, from the current date in UTC. Use UTC when records from users in different time zones must be grouped into the same month.

```
var gdt = mgs.nowGlideDateTime();
        var month = gdt.getMonthUTC();
        var key = gdt.getYearUTC() + '-' + (month < 10 ? '0' + month : month);
        mgs.info(key);
```

Output:

```
2026-08
```

## MobileGlideDateTime - getNumericValue\(\)

Gets the date and time value as the number of milliseconds since January 1, 1970, 00:00:00 GMT. Use this method to compare, sort, or calculate the time between date and time values.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getNumericValue_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of milliseconds that have elapsed since January 1, 1970, 00:00:00 GMT.Unit: milliseconds

</td></tr></tbody>
</table>This example gets the current date and time as the number of milliseconds since January 1, 1970, 00:00:00 GMT and logs it.

```
mgs.info(mgs.nowGlideDateTime().getNumericValue());
```

Output:

```
1787855057000
```

This example builds a unique reference from the current date and time. The numeric value also works as a sort key, because later values are always larger.

```
var stamp = mgs.nowGlideDateTime().getNumericValue();
        mgs.info('REQ-' + stamp);
```

Output:

```
REQ-1787855057000
```

## MobileGlideDateTime - getTime\(\) / getLocalTime\(\)

Gets the time-of-day portion of this date and time. getTime\(\) returns the time in the system time zone, and getLocalTime\(\) returns it in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md)|MobileGlideTime object that contains the hours, minutes, and seconds of the date and time value, with no date. For the methods that you can call on this object, see the reference for [MobileGlideTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md).|

This example checks whether the current time falls within a maintenance window that’s defined in UTC, from 20:00 to 22:00. A button condition can use this check to hide a Sync now button during maintenance.

```
var hour = mgs.nowGlideDateTime().getTime().getHourOfDayUTC();
        var inMaintenance = hour >= 20 && hour < 22;
        mgs.info('In maintenance window: ' + inMaintenance);
```

Output:

```
In maintenance window: true
```

This example gets the time portion of the current date and time in the user’s time zone and logs the hour of the day.

```
var time = mgs.nowGlideDateTime().getLocalTime();
mgs.info(time.getHourOfDayLocalTime());
```

Output:

```
16
```

This example checks whether the current local time is within business hours. A button condition can use this check to show a Call dispatch button only from 8:00 AM to 5:00 PM.

```
var hour = mgs.nowGlideDateTime().getLocalTime().getHourOfDayLocalTime();
        var isBusinessHours = hour >= 8 && hour < 17;
        mgs.info('Within business hours: ' + isBusinessHours);
```

Output:

```
Within business hours: true
```

## MobileGlideDateTime - getTZOffset\(\)

Gets the offset between the time zone and UTC, in milliseconds.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getTZOffset_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Time zone offset. Unit: milliseconds

</td></tr></tbody>
</table>This example gets the time zone offset, in milliseconds, and logs it.

```
mgs.info(mgs.nowGlideDateTime().getTZOffset());
```

This example converts the time zone offset to hours and builds a readable UTC label, such as to show users which time zone a timestamp uses.

```
var hours = mgs.nowGlideDateTime().getTZOffset() / (60 * 60 * 1000);
        var label = 'UTC' + (hours >= 0 ? '+' : '') + hours;
        mgs.info('Times shown in ' + label);
```

Output:

```
Times shown in UTC-4
```

## MobileGlideDateTime - getUserFormattedLocalTime\(\) / getInternalFormattedLocalTime\(\)

Gets the date and time in the current user's time zone. getUserFormattedLocalTime\(\) returns the value in the user's display format, and getInternalFormattedLocalTime\(\) returns it in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getUserFormattedLocalTime_getInternalFormattedLocalTime_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date and time in the current user's time zone, in the user's display format or the internal format, depending on the method called.-   getUserFormattedLocalTime\(\): Value in the user’s date and time display format, such as 08/26/2026 16:44:17.
-   getInternalFormattedLocalTime\(\): Value in the internal format, yyyy-MM-dd HH:mm:ss, such as 2026-08-26 16:44:17.

</td></tr></tbody>
</table>This example gets the current date and time in the user’s time zone and display format and logs it.

```
mgs.info(mgs.nowGlideDateTime().getUserFormattedLocalTime());
```

Output:

```
08/26/2026 16:44:17
```

This example builds a check-in message with the local time in the user’s display format. Use getInternalFormattedLocalTime\(\) instead when the value is stored or compared.

```
var checkIn = mgs.nowGlideDateTime().getUserFormattedLocalTime();
        mgs.info('Checked in at ' + checkIn);
```

Output:

```
Checked in at 08/26/2026 16:44:17
```

This example builds a check-in reference from the user’s local date and time in the internal format, which stays the same regardless of the user’s date format preference.

```
var checkIn = mgs.nowGlideDateTime().getInternalFormattedLocalTime();
        mgs.info('CHECKIN-' + checkIn);
```

Output:

```
CHECKIN-2026-08-26 16:44:17
```

## MobileGlideDateTime - getValue\(\) / getDisplayValue\(\) / getDisplayValueInternal\(\)

Gets the date-time value. getValue\(\) returns the internal-format value; getDisplayValue\(\) returns the current user's display-format value; getDisplayValueInternal\(\) returns the display value expressed in the internal format.

Use getValue\(\) for values that you store or compare, getDisplayValue\(\) for text that users read, and getDisplayValueInternal\(\) when you need the user’s local date and time in a consistent format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getValue_getDisplayValue_getDisplayValueInternal_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date and time value as a string, in the format for the method called.-   getValue\(\): Value in the internal format, yyyy-MM-dd HH:mm:ss, in UTC, such as 2026-08-26 20:44:17.
-   getDisplayValue\(\): Value in the current user’s date and time display format and time zone, such as 08/26/2026 16:44:17.
-   getDisplayValueInternal\(\): Value in the internal format, yyyy-MM-dd HH:mm:ss, in the current user’s time zone, such as 2026-08-26 16:44:17.

</td></tr></tbody>
</table>This example gets the current date and time in the internal format and logs it.

```
var gdt = mgs.nowGlideDateTime();
mgs.info(gdt.getValue());
```

Output:

```
"2026-08-26 20:44:17"
```

This example gets the current date and time in the user’s time zone, in the internal format. Unlike getDisplayValue\(\), the format is the same for every user.

```
var gdt = mgs.nowGlideDateTime();
        mgs.info(gdt.getDisplayValueInternal());
```

Output:

```
2026-08-26 16:44:17
```

This example gets the current date and time in two formats. The internal-format value is for storing or comparing. The display-format value, in the user’s time zone, is for text that users read.

```
var gdt = mgs.nowGlideDateTime();
        var storedValue = gdt.getValue();
        var displayText = 'Last updated ' + gdt.getDisplayValue();
        mgs.info(storedValue);
        mgs.info(displayText);
```

Output:

```
2026-08-26 20:44:17
        Last updated 08/26/2026 16:44:17
```

## MobileGlideDateTime - getWeekOfYearLocalTime\(\) / getWeekOfYearUTC\(\)

Gets the number of the week in the year. getWeekOfYearLocalTime\(\) returns the week in the user's time zone, and getWeekOfYearUTC\(\) returns the week in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-getWeekOfYearLocalTime_getWeekOfYearUTC_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Week of the year. Range: 1-53

</td></tr></tbody>
</table>This example gets the current week of the year, in the user’s time zone, and logs it.

```
mgs.info(mgs.nowGlideDateTime().getWeekOfYearLocalTime());
```

Output:

```
35
```

This example builds a weekly report label from the current week and year.

```
var gdt = mgs.nowGlideDateTime();
        mgs.info('Week ' + gdt.getWeekOfYearLocalTime() + ' of ' + gdt.getYearLocalTime());
```

Output:

```
Week 35 of 2026
```

This example gets the current week of the year in UTC, such as to label a weekly report that covers users in several time zones.

```
var week = mgs.nowGlideDateTime().getWeekOfYearUTC();
        mgs.info('Weekly report: week ' + week + ' (UTC)');
```

Output:

```
Weekly report: week 35 (UTC)
```

## MobileGlideDateTime - getYearLocalTime\(\) / getYearUTC\(\)

Gets the four-digit year of this date and time. getYearLocalTime\(\) returns the value in the current user's time zone and getYearUTC\(\) returns the value in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Four-digit year in the current user's time zone for getYearLocalTime\(\) or in UTC for getYearUTC\(\).|

This example builds an archive reference from the current year in UTC, so the reference is the same for users in every time zone.

```
var year = mgs.nowGlideDateTime().getYearUTC();
        mgs.info('ARCHIVE-' + year);
```

Output:

```
ARCHIVE-2026
```

This example gets the current four-digit year, in the user's time zone, and logs it.

```
mgs.info(mgs.nowGlideDateTime().getYearLocalTime());
```

Output:

```
2026
```

This example calculates an asset's age in years from its model year. The asset's model year is 2021.

```
var currentYear = mgs.nowGlideDateTime().getYearLocalTime();
        var modelYear = parseInt(current.model_year.getValue(), 10);
        mgs.info('Asset age: ' + (currentYear - modelYear) + ' years');
```

Output:

```
Asset age: 5 years
```

## MobileGlideDateTime - isDST\(\)

Determines whether this datetime uses a daylight saving offset.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-isDST_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether daylight saving is in effect. Possible values:

-   true: Daylight saving is in effect.
-   false:Daylight saving is not in effect.

</td></tr></tbody>
</table>This example checks whether daylight saving time is in effect for the current date and time and logs the result.

```
mgs.info(mgs.nowGlideDateTime().isDST());
```

Output:

```
false
```

This example logs a message that tells users whether times are shown in daylight saving time or standard time.

```
var label = mgs.nowGlideDateTime().isDST() ? 'daylight saving time' : 'standard time';
        mgs.info('Times are shown in ' + label);
```

Output:

```
Times are shown in standard time
```

## MobileGlideDateTime - isValid\(\)

Determines whether the value is a valid date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGDT-isValid_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the value is a valid date-time.Possible values:

-   true: This is a valid date-time.
-   false: This is not a valid date-time.

</td></tr></tbody>
</table>This example checks whether the current date and time is a valid value and logs the result.

```
mgs.info(mgs.nowGlideDateTime().isValid());
```

Output:

```
true
```

This example checks that a date and time value is valid before the script records it. A write-back action can use this check to avoid saving an invalid check-in time.

```
var gdt = mgs.nowGlideDateTime();
        if (gdt.isValid()) {
        mgs.info('Check-in time: ' + gdt.getDisplayValue());
        } else {
        mgs.info('Invalid date and time. Check-in not recorded.');
        }
```

Output:

```
Check-in time: 08/26/2026 16:44:17
```

## MobileGlideDateTime - toString\(\)

Gets the date and time value as a string in the internal format, yyyy-MM-dd HH:mm:ss, such as for adding the value to a log message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date and time value in the internal format, yyyy-MM-dd HH:mm:ss, in UTC, such as 2026-08-26 20:44:17.|

This example converts the current date and time to a string and logs it.

```
mgs.info(String(mgs.nowGlideDateTime()));
```

Output:

```
2026-08-26 20:44:17
```

This example adds the current date and time to a log message.

```
var gdt = mgs.nowGlideDateTime();
        mgs.info('Record updated at ' + gdt.toString());
```

Output:

```
Record updated at 2026-08-26 20:44:17
```

