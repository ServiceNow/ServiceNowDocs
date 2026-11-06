---
title: MobileGlideSystem - Scoped
description: The MobileGlideSystem API provides utility methods for the current session, including user information, date and time values, and script logging.Shows a specified error message to the user in the mobile client for the current session.Shows an informational message to the user in the mobile client for the current session.Gets the UTC date and time at the start or end of the day that contains a given date and time.Gets the UTC start or end of a named relative date range, such as this month, last quarter, or yesterday.Generates a date and time string from a date and a time of day, such as the start or end of a day or a specific time.Gets the translated message for the given message ID, substituting positional placeholders in the message text.Gets a read-only MobileGlideUser object for the current user.Gets the display name of the current user, such as the name shown on records.Gets the sys\_id of the current user.Gets the user name that the current user logs in with.Determines whether the current user has a specific role. A condition script can use this check to show or hide a button based on the user's role.Writes an informational message to the system log, such as to check how a script runs. To show a message to the user, use addInfoMessage\(\).Gets a date and time a number of units in the past. The unitAgo\(\) methods return the exact moment, the unitAgoStart\(\) methods return the start of that period, and the unitAgoEnd\(\) methods return the end of it.Determines whether the value is null, undefined, or an empty string.Gets the current date, with no time of day. To get the date and time, use nowDateTime\(\).Gets the current date and time in the user's time zone and display format.Gets a MobileGlideDateTime object for the current date and time. Use the object's methods to read or compare parts of the date and time.Gets the current date and time in UTC, in the internal format, with no time zone conversion.Gets the date and time 24 hours ago \(yesterday\(\)\) or 7 days ago \(lastWeek\(\)\), in the internal format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileGlideSystemScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 30
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideSystem - Scoped

The MobileGlideSystem API provides utility methods for the current session, including user information, date and time values, and script logging.

MobileGlideSystem methods provide the subset of GlideSystem behavior that can be evaluated against the local database on a device: identity and role checks for the current user, and logging and messaging. Most of the class consists of date-range helpers that mirror the GlideSystem date-range shortcuts used in filters and reports, such as the beginning of the previous quarter. These helpers let a script express a relative time window without calculating dates directly.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

This API contains the following capabilities:

-   Logging messages: [MobileGlideSystem - info\(String message\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md)
-   Showing messages to users: [MobileGlideSystem - addInfoMessage\(String message\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - addErrorMessage\(String error\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - getMessage\(String messageId, Object args\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md)
-   Getting information about the current user: [MobileGlideSystem - getUser\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - getUserID\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - getUserName\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - getUserDisplayName\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - hasRole\(String role\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md)
-   Getting and creating date and time values: [MobileGlideSystem - now\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - nowDateTime\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - nowNoTZ\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - nowGlideDateTime\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - dateGenerate\(String date, String range\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md)
-   Getting relative dates and times: [MobileGlideSystem - yesterday\(\) / lastWeek\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - minutesAgo\(n\) / hoursAgo\(n\) / daysAgo\(n\) / monthsAgo\(n\) / quartersAgo\(n\) / yearsAgo\(n\) — N-units-ago](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md)
-   Getting the start and end of date ranges: [MobileGlideSystem - beginningOfDay\(MobileGlideDateTime dateTime\) / endOfDay\(MobileGlideDateTime dateTime\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md), [MobileGlideSystem - beginningOfX\(\) / endOfX\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md)
-   Checking for empty values: [MobileGlideSystem - nil\(Object value\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md)

For guidance on date time input strings with a list of common format conflicts, refer to [Server-side script use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/useful-server-side-scripts.md).

## API Access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class can't be instantiated. All members are static delegates, and the class is accessed through the variable `mgs`, which the mobile scripting preamble declares as `var mgs = sn_mobile_scripting.MobileGlideSystem;`.

## MobileGlideSystem - addErrorMessage\(String error\)

Shows a specified error message to the user in the mobile client for the current session.

|Name|Type|Description|
|----|----|-----------|
|error|String|Error text to display to the user.|

|Type|Description|
|----|-----------|
|void| |

This example shows an error message that explains why a field can't be edited.

```
mgs.addErrorMessage('This field cannot be edited while the record is closed.');
```

This example checks the state of the current task and shows an error message if the task is closed. The state value for a closed task is 3. A write-back action can use this check to explain why a change wasn't made.

```
if (current.getValue('state') === '3') {
        mgs.addErrorMessage('Task ' + current.getValue('number') + ' is closed and cannot be edited.');
        }
```

## MobileGlideSystem - addInfoMessage\(String message\)

Shows an informational message to the user in the mobile client for the current session.

|Name|Type|Description|
|----|----|-----------|
|message|String|Text to display to the user.|

|Type|Description|
|----|-----------|
|void| |

This example shows a message that confirms a record was saved.

```
mgs.addInfoMessage('Your changes were saved.');
```

This example creates a follow-up task and shows the user a message that depends on the result. Use addErrorMessage\(\) to show a failure so that the user can tell the two outcomes apart.

```
var gr = new MobileGlideRecord('wm_task');
        gr.initialize();
        gr.setValue('parent', current.getValue('sys_id'));
        gr.setValue('short_description', 'Follow-up required');
        if (gr.insert()) {
        mgs.addInfoMessage('Follow-up task created.');
        } else {
        mgs.addErrorMessage('The follow-up task could not be created.');
        }
```

## MobileGlideSystem - beginningOfDay\(MobileGlideDateTime dateTime\) / endOfDay\(MobileGlideDateTime dateTime\)

Gets the UTC date and time at the start or end of the day that contains a given date and time.

Unlike the fixed named-range methods, this method takes a [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md) parameter rather than being parameterless.

|Name|Type|Description|
|----|----|-----------|
|dateTime|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)|The date-time whose containing day's start/end is returned.|

|Type|Description|
|----|-----------|
|String|UTC date and time at the start \(beginningOfDay\(\)\) or end \(endOfDay\(\)\) of the day that contains `dateTime`, in the format `yyyy-MM-dd HH:mm:ss`.|

This example gets the start of the day that contains the current date and time and logs it.

```
var dayStart = mgs.beginningOfDay(mgs.nowGlideDateTime());
        mgs.info(dayStart);
```

Output:

```
2026-08-26 00:00:00
```

This example counts the tasks that were created during the current day, such as for a daily summary.

```
var now = mgs.nowGlideDateTime();
        var dayStart = mgs.beginningOfDay(now);
        var dayEnd = mgs.endOfDay(now);
        var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('sys_created_onBETWEEN' + dayStart + '@' + dayEnd);
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('Tasks created today: ' + count);
```

Output:

```
Tasks created today: 2
```

This example checks whether a record’s due date falls on or before the end of the current day. A button condition can use this check to show a Mark as urgent button for tasks that are due today or overdue.

```
var endOfToday = mgs.endOfDay(mgs.nowGlideDateTime());
        var due = current.due_date.getValue();
        var dueByEndOfDay = due <= endOfToday;
        mgs.info('Due by end of day: ' + dueByEndOfDay);
```

Output:

```
Due by end of day: false
```

## MobileGlideSystem - beginningOfX\(\) / endOfX\(\)

Gets the UTC start or end of a named relative date range, such as this month, last quarter, or yesterday.

The example after the table uses beginningOfThisMonth\(\) and endOfThisMonth\(\). The other pairs work the same way and differ only in the date range.

All beginningOfX\(\)/endOfX\(\) pairs in this family:

-   beginningOfLast3Months\(\) / endOfLast3Months\(\)
-   beginningOfLast6Months\(\) / endOfLast6Months\(\)
-   beginningOfLast9Months\(\) / endOfLast9Months\(\)
-   beginningOfLast12Months\(\) / endOfLast12Months\(\)
-   beginningOfLastQuarter\(\) / endOfLastQuarter\(\)
-   beginningOfLast2Quarters\(\) / endOfLast2Quarters\(\)
-   beginningOfNextQuarter\(\) / endOfNextQuarter\(\)
-   beginningOfNext2Quarters\(\) / endOfNext2Quarters\(\)
-   beginningOfLast2Years\(\) / endOfLast2Years\(\)
-   beginningOfLast7Days\(\) / endOfLast7Days\(\)
-   beginningOfLast30Days\(\) / endOfLast30Days\(\)
-   beginningOfLast60Days\(\) / endOfLast60Days\(\)
-   beginningOfLast90Days\(\) / endOfLast90Days\(\)
-   beginningOfLast120Days\(\) / endOfLast120Days\(\)
-   beginningOfCurrentHour\(\) / endOfCurrentHour\(\)
-   beginningOfLastHour\(\) / endOfLastHour\(\)
-   beginningOfLast2Hours\(\) / endOfLast2Hours\(\)
-   beginningOfCurrentMinute\(\) / endOfCurrentMinute\(\)
-   beginningOfLastMinute\(\) / endOfLastMinute\(\)
-   beginningOfLast15Minutes\(\) / endOfLast15Minutes\(\)
-   beginningOfLast30Minutes\(\) / endOfLast30Minutes\(\)
-   beginningOfLast45Minutes\(\) / endOfLast45Minutes\(\)
-   beginningOfOneYearAgo\(\) / endOfOneYearAgo\(\)
-   beginningOfToday\(\) / endOfToday\(\)
-   beginningOfYesterday\(\) / endOfYesterday\(\)
-   beginningOfTomorrow\(\) / endOfTomorrow\(\)
-   beginningOfThisWeek\(\) / endOfThisWeek\(\)
-   beginningOfLastWeek\(\) / endOfLastWeek\(\)
-   beginningOfNextWeek\(\) / endOfNextWeek\(\)
-   beginningOfThisMonth\(\) / endOfThisMonth\(\)
-   beginningOfLastMonth\(\) / endOfLastMonth\(\)
-   beginningOfNextMonth\(\) / endOfNextMonth\(\)
-   beginningOfThisQuarter\(\) / endOfThisQuarter\(\)
-   beginningOfThisYear\(\) / endOfThisYear\(\)
-   beginningOfLastYear\(\) / endOfLastYear\(\)
-   beginningOfNextYear\(\) / endOfNextYear\(\)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|UTC date and time at the start or end of the named range, in the format `yyyy-MM-dd HH:mm:ss`.|

This example gets the first and last moments of the current month and logs them as a range.

```
var start = mgs.beginningOfThisMonth();
        var end = mgs.endOfThisMonth();
        mgs.info(start + ' to ' + end);
```

Output:

```
2026-08-01 00:00:00 to 2026-08-31 23:59:59
```

This example counts the tasks that were created last month, such as for a monthly report.

```
var start = mgs.beginningOfLastMonth();
        var end = mgs.endOfLastMonth();
        var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('sys_created_onBETWEEN' + start + '@' + end);
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('Tasks created last month: ' + count);
```

Output:

```
Tasks created last month: 14
```

This example uses beginningOfLast3Months\(\) and endOfLast3Months\(\) to count the tasks that were closed in the last three months, such as for a quarterly summary.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('closed_atBETWEEN' + mgs.beginningOfLast3Months() + '@' + mgs.endOfLast3Months());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks closed in the last 3 months: ' + count);
```

Output:

```
Tasks closed in the last 3 months: 42
```

This example uses beginningOfLast6Months\(\) and endOfLast6Months\(\) to count the tasks that were created in the last six months, such as for a half-year report.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast6Months() + '@' + mgs.endOfLast6Months());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 6 months: ' + count);
```

Output:

```
Tasks created in the last 6 months: 87
```

This example uses beginningOfLast9Months\(\) and endOfLast9Months\(\) to count the tasks that were created in the last nine months, such as for a review that covers three quarters.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast9Months() + '@' + mgs.endOfLast9Months());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 9 months: ' + count);
```

Output:

```
Tasks created in the last 9 months: 130
```

This example uses beginningOfLast12Months\(\) and endOfLast12Months\(\) to count the tasks that were created in the last 12 months, such as for an annual summary.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast12Months() + '@' + mgs.endOfLast12Months());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 12 months: ' + count);
```

Output:

```
Tasks created in the last 12 months: 176
```

This example uses beginningOfLastQuarter\(\) and endOfLastQuarter\(\) to get the first and last moments of the previous quarter and logs them as a range.

```
var start = mgs.beginningOfLastQuarter();
var end = mgs.endOfLastQuarter();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-04-01 00:00:00 to 2026-06-30 23:59:59
```

This example uses beginningOfLast2Quarters\(\) and endOfLast2Quarters\(\) to count the tasks that were closed in the last two quarters.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('closed_atBETWEEN' + mgs.beginningOfLast2Quarters() + '@' + mgs.endOfLast2Quarters());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks closed in the last 2 quarters: ' + count);
```

Output:

```
Tasks closed in the last 2 quarters: 61
```

This example uses beginningOfNextQuarter\(\) and endOfNextQuarter\(\) to get the first and last moments of the next quarter and logs them as a range, such as for a planning view.

```
var start = mgs.beginningOfNextQuarter();
var end = mgs.endOfNextQuarter();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-10-01 00:00:00 to 2026-12-31 23:59:59
```

This example uses beginningOfNext2Quarters\(\) and endOfNext2Quarters\(\) to check whether a record’s due date falls within the next two quarters. A button condition can use this check to show a Plan work button for upcoming tasks.

```
var due = current.due_date.getValue();
var inRange = due >= mgs.beginningOfNext2Quarters() && due <= mgs.endOfNext2Quarters();
mgs.info('Due in the next 2 quarters: ' + inRange);
```

Output:

```
Due in the next 2 quarters: true
```

This example uses beginningOfLast2Years\(\) and endOfLast2Years\(\) to count the tasks that were created in the last two years.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast2Years() + '@' + mgs.endOfLast2Years());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 2 years: ' + count);
```

Output:

```
Tasks created in the last 2 years: 305
```

This example uses beginningOfLast7Days\(\) and endOfLast7Days\(\) to count the tasks that were closed in the last seven days, such as for a weekly summary.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('closed_atBETWEEN' + mgs.beginningOfLast7Days() + '@' + mgs.endOfLast7Days());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks closed in the last 7 days: ' + count);
```

Output:

```
Tasks closed in the last 7 days: 9
```

This example uses beginningOfLast30Days\(\) and endOfLast30Days\(\) to count the tasks that were created in the last 30 days.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast30Days() + '@' + mgs.endOfLast30Days());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 30 days: ' + count);
```

Output:

```
Tasks created in the last 30 days: 23
```

This example uses beginningOfLast60Days\(\) and endOfLast60Days\(\) to check whether a record was updated in the last 60 days. A button condition can use this check to show a Request review button only for records that haven’t been updated recently.

```
var updated = current.sys_updated_on.getValue();
var recentlyUpdated = updated >= mgs.beginningOfLast60Days() && updated <= mgs.endOfLast60Days();
mgs.info('Show Request review button: ' + !recentlyUpdated);
```

Output:

```
Show Request review button: false
```

This example uses beginningOfLast90Days\(\) and endOfLast90Days\(\) to count the tasks that were closed in the last 90 days.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('closed_atBETWEEN' + mgs.beginningOfLast90Days() + '@' + mgs.endOfLast90Days());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks closed in the last 90 days: ' + count);
```

Output:

```
Tasks closed in the last 90 days: 38
```

This example uses beginningOfLast120Days\(\) and endOfLast120Days\(\) to count the tasks that were created in the last 120 days.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast120Days() + '@' + mgs.endOfLast120Days());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 120 days: ' + count);
```

Output:

```
Tasks created in the last 120 days: 51
```

This example uses beginningOfCurrentHour\(\) and endOfCurrentHour\(\) to get the first and last moments of the current hour and logs them as a range.

```
var start = mgs.beginningOfCurrentHour();
var end = mgs.endOfCurrentHour();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-08-26 20:00:00 to 2026-08-26 20:59:59
```

This example uses beginningOfLastHour\(\) and endOfLastHour\(\) to count the tasks that were updated during the previous hour.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_updated_onBETWEEN' + mgs.beginningOfLastHour() + '@' + mgs.endOfLastHour());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks updated in the last hour: ' + count);
```

Output:

```
Tasks updated in the last hour: 2
```

This example uses beginningOfLast2Hours\(\) and endOfLast2Hours\(\) to count the tasks that were created in the last two hours.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast2Hours() + '@' + mgs.endOfLast2Hours());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 2 hours: ' + count);
```

Output:

```
Tasks created in the last 2 hours: 3
```

This example uses beginningOfCurrentMinute\(\) and endOfCurrentMinute\(\) to get the first and last moments of the current minute and logs them as a range.

```
var start = mgs.beginningOfCurrentMinute();
var end = mgs.endOfCurrentMinute();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-08-26 20:44:00 to 2026-08-26 20:44:59
```

This example uses beginningOfLastMinute\(\) and endOfLastMinute\(\) to get the first and last moments of the previous minute and logs them as a range.

```
var start = mgs.beginningOfLastMinute();
var end = mgs.endOfLastMinute();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-08-26 20:43:00 to 2026-08-26 20:43:59
```

This example uses beginningOfLast15Minutes\(\) and endOfLast15Minutes\(\) to count the tasks that were updated in the last 15 minutes.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_updated_onBETWEEN' + mgs.beginningOfLast15Minutes() + '@' + mgs.endOfLast15Minutes());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks updated in the last 15 minutes: ' + count);
```

Output:

```
Tasks updated in the last 15 minutes: 1
```

This example uses beginningOfLast30Minutes\(\) and endOfLast30Minutes\(\) to check whether a record was updated in the last 30 minutes. A button condition can use this check to show an Undo last change button only shortly after an update.

```
var updated = current.sys_updated_on.getValue();
var recentlyUpdated = updated >= mgs.beginningOfLast30Minutes() && updated <= mgs.endOfLast30Minutes();
mgs.info('Show Undo last change button: ' + recentlyUpdated);
```

Output:

```
Show Undo last change button: false
```

This example uses beginningOfLast45Minutes\(\) and endOfLast45Minutes\(\) to count the tasks that were created in the last 45 minutes.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLast45Minutes() + '@' + mgs.endOfLast45Minutes());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created in the last 45 minutes: ' + count);
```

Output:

```
Tasks created in the last 45 minutes: 1
```

This example uses beginningOfOneYearAgo\(\) and endOfOneYearAgo\(\) to count the tasks that were created on the same day last year, such as to compare current activity with the same day a year earlier.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfOneYearAgo() + '@' + mgs.endOfOneYearAgo());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created on this day last year: ' + count);
```

Output:

```
Tasks created on this day last year: 2
```

This example uses beginningOfToday\(\) and endOfToday\(\) to check whether a record’s due date falls on the current day. A button condition can use this check to show a Due today badge.

```
var due = current.due_date.getValue();
var dueToday = due >= mgs.beginningOfToday() && due <= mgs.endOfToday();
mgs.info('Due today: ' + dueToday);
```

Output:

```
Due today: false
```

This example uses beginningOfYesterday\(\) and endOfYesterday\(\) to count the tasks that were closed during the previous day, such as for a daily summary.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('closed_atBETWEEN' + mgs.beginningOfYesterday() + '@' + mgs.endOfYesterday());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks closed yesterday: ' + count);
```

Output:

```
Tasks closed yesterday: 5
```

This example uses beginningOfTomorrow\(\) and endOfTomorrow\(\) to check whether a record’s due date falls on the next day. A button condition can use this check to show a Send reminder button.

```
var due = current.due_date.getValue();
var dueTomorrow = due >= mgs.beginningOfTomorrow() && due <= mgs.endOfTomorrow();
mgs.info('Show Send reminder button: ' + dueTomorrow);
```

Output:

```
Show Send reminder button: true
```

This example uses beginningOfThisWeek\(\) and endOfThisWeek\(\) to get the first and last moments of the current week and logs them as a range.

```
var start = mgs.beginningOfThisWeek();
var end = mgs.endOfThisWeek();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-08-24 00:00:00 to 2026-08-30 23:59:59
```

This example uses beginningOfLastWeek\(\) and endOfLastWeek\(\) to count the tasks that were created during the previous week, such as for a weekly report.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLastWeek() + '@' + mgs.endOfLastWeek());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created last week: ' + count);
```

Output:

```
Tasks created last week: 11
```

This example uses beginningOfNextWeek\(\) and endOfNextWeek\(\) to check whether a record’s due date falls within the next week. A button condition can use this check to show a Schedule for next week button.

```
var due = current.due_date.getValue();
var dueNextWeek = due >= mgs.beginningOfNextWeek() && due <= mgs.endOfNextWeek();
mgs.info('Show Schedule for next week button: ' + dueNextWeek);
```

Output:

```
Show Schedule for next week button: false
```

This example uses beginningOfNextMonth\(\) and endOfNextMonth\(\) to get the first and last moments of the next month and logs them as a range.

```
var start = mgs.beginningOfNextMonth();
var end = mgs.endOfNextMonth();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-09-01 00:00:00 to 2026-09-30 23:59:59
```

This example uses beginningOfThisQuarter\(\) and endOfThisQuarter\(\) to count the tasks that were closed during the current quarter.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('closed_atBETWEEN' + mgs.beginningOfThisQuarter() + '@' + mgs.endOfThisQuarter());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks closed this quarter: ' + count);
```

Output:

```
Tasks closed this quarter: 27
```

This example uses beginningOfThisYear\(\) and endOfThisYear\(\) to get the first and last moments of the current year and logs them as a range.

```
var start = mgs.beginningOfThisYear();
var end = mgs.endOfThisYear();
mgs.info(start + ' to ' + end);
```

Output:

```
2026-01-01 00:00:00 to 2026-12-31 23:59:59
```

This example uses beginningOfLastYear\(\) and endOfLastYear\(\) to count the tasks that were created during the previous year, such as for a year-over-year comparison.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('sys_created_onBETWEEN' + mgs.beginningOfLastYear() + '@' + mgs.endOfLastYear());
gr.query();
var count = 0;
while (gr.next()) {
  count++;
}
mgs.info('Tasks created last year: ' + count);
```

Output:

```
Tasks created last year: 198
```

This example uses beginningOfNextYear\(\) and endOfNextYear\(\) to check whether a record’s due date falls within the next year. A button condition can use this check to show a Defer to next year button.

```
var due = current.due_date.getValue();
var dueNextYear = due >= mgs.beginningOfNextYear() && due <= mgs.endOfNextYear();
mgs.info('Show Defer to next year button: ' + dueNextYear);
```

Output:

```
Show Defer to next year button: false
```

## MobileGlideSystem - dateGenerate\(String date, String range\)

Generates a date and time string from a date and a time of day, such as the start or end of a day or a specific time.

|Name|Type|Description|
|----|----|-----------|
|date|String|Date in `yyyymmdd` format, such as `20260215`.|
|range|String|Time of day for the returned value. Valid values: `start` for 00:00:00, `end` for 23:59:59, or a specific time in `hh:mm:ss` 24-hour format.|

|Type|Description|
|----|-----------|
|String|Date and time string, such as `2026-02-15 00:00:00`.|

This example gets the start of February 15, 2026 and logs it.

```
var rangeStart = mgs.dateGenerate('20260215', 'start');
        mgs.info(rangeStart);
```

Output:

```
2026-02-15 00:00:00
```

This example sets the due date of a new task to 5:00 PM on a given day and logs the stored value.

```
var gr = new MobileGlideRecord('wm_task');
        gr.initialize();
        gr.setValue('short_description', 'Replace filter');
        gr.setValue('due_date', mgs.dateGenerate('20260901', '17:00:00'));
        mgs.info(gr.getValue('due_date'));
```

Output:

```
2026-09-01 17:00:00
```

## MobileGlideSystem - getMessage\(String messageId, Object args\)

Gets the translated message for the given message ID, substituting positional placeholders in the message text.

|Name|Type|Description|
|----|----|-----------|
|messageId|String|Key of the message in the Messages \[sys\_ui\_message\] table. If no message matches the key, the method returns the key itself as the message text.|
|args|Object|Optional. A value, or an array of values, to insert into the placeholders `{0}`, `{1}`, and so on, in the message text, in order.|

|Type|Description|
|----|-----------|
|String|Translated message text with the values inserted. If no message matches the key, the key is returned as the text.|

This example passes message text that contains a placeholder, along with one value. No message record matches this text, so the method uses the text as the message and inserts the value.

```
mgs.info(mgs.getMessage('This {0} record is currently locked.', ['incident']));
```

Output:

```
This incident record is currently locked.
```

This example gets a message by its key and fills in the task number and the user's name, then shows it to the user. It assumes a message record with the key `task_assigned` and the text `Task {0} was assigned to {1}.` The user sees the message in their own language if a translation exists.

```
var message = mgs.getMessage('task_assigned', [current.getValue('number'), mgs.getUserDisplayName()]);
        mgs.addInfoMessage(message);
```

Output:

```
Task WM0001001 was assigned to Jordan Alvarez.
```

## MobileGlideSystem - getUser\(\)

Gets a read-only MobileGlideUser object for the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideUser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md)|Object for the current user. For its available methods, see [MobileGlideUser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md).|

This example gets the display name of the current user from the MobileGlideUser object and logs it.

```
var displayName = mgs.getUser().getDisplayName();
        mgs.info(displayName);
```

Output:

```
Jane Doe
```

This example gets the MobileGlideUser object once and uses it to build a message that records who completed an inspection.

```
var user = mgs.getUser();
        var note = 'Inspection completed by ' + user.getDisplayName();
        mgs.info(note);
```

Output:

```
Inspection completed by Jane Doe
```

## MobileGlideSystem - getUserDisplayName\(\)

Gets the display name of the current user, such as the name shown on records.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display name of the current user, such as `Jane Doe`.|

This example gets the display name of the current user and logs it.

```
mgs.info(mgs.getUserDisplayName());
```

Output:

```
Jane Doe
```

This example builds a note that records who completed an inspection and on what date.

```
var note = 'Inspection completed by ' + mgs.getUserDisplayName() + ' on ' + mgs.now();
        mgs.info(note);
```

Output:

```
Inspection completed by Jane Doe on 08/26/2026
```

## MobileGlideSystem - getUserID\(\)

Gets the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current user.|

This example gets the sys\_id of the current user and logs it.

```
mgs.info(mgs.getUserID());
```

Output:

```
62826bf03710200044e0bfc8bcbe5dec
```

This example checks whether the current user is the user assigned to the task. A button condition can use this check to show a Start work button only to the assignee.

```
var isAssignee = current.getValue('assigned_to') === mgs.getUserID();
        mgs.info('Show Start work button: ' + isAssignee);
```

Output:

```
Show Start work button: true
```

## MobileGlideSystem - getUserName\(\)

Gets the user name that the current user logs in with.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User name of the current user, such as `employee.smith`.|

This example gets the user name of the current user and logs it.

```
mgs.info(mgs.getUserName());
```

Output:

```
employee.smith
```

This example adds the user name to a log message so that the log shows who ran the script, such as when troubleshooting a button condition.

```
mgs.info('[' + mgs.getUserName() + '] Condition evaluated for record ' + current.getValue('number'));
```

Output:

```
[employee.smith] Condition evaluated for record WM0001001
```

## MobileGlideSystem - hasRole\(String role\)

Determines whether the current user has a specific role. A condition script can use this check to show or hide a button based on the user's role.

|Name|Type|Description|
|----|----|-----------|
|role|String|Name of the role to check, such as `itil`.|

<table id="table_MGS-hasRole_S_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user has the specified role.Possible values:

-   true: User has the role.
-   false: User does not have the role.

</td></tr></tbody>
</table>This example checks whether the current user has the itil role and logs a message if they do.

```
if (mgs.hasRole('itil')) {
        mgs.info('User is ITIL');
        }
```

Output:

```
User is ITIL
```

This example checks whether the current user is a dispatcher or an administrator. A button condition can use this check to show a Reassign button only to those users.

```
var canReassign = mgs.hasRole('wm_dispatcher') || mgs.hasRole('admin');
        mgs.info('Show Reassign button: ' + canReassign);
```

Output:

```
Show Reassign button: true
```

## MobileGlideSystem - info\(String message\)

Writes an informational message to the system log, such as to check how a script runs. To show a message to the user, use addInfoMessage\(\).

|Name|Type|Description|
|----|----|-----------|
|message|String|Text to write to the system log.|

|Type|Description|
|----|-----------|
|void| |

This example logs the sys\_id of the current record from a condition script, to confirm when the condition runs.

```
mgs.info('Condition evaluated for record ' + current.getValue('sys_id'));
```

This example logs the values that a button condition depends on, so the log shows why the button appeared or didn't.

```
var state = current.getValue('state');
        var assignee = current.getValue('assigned_to');
        mgs.info('Button condition: state=' + state + ', assigned_to=' + assignee);
```

Output written to the log:

```
Button condition: state=2, assigned_to=62826bf03710200044e0bfc8bcbe5dec
```

## MobileGlideSystem - minutesAgo\(n\) / hoursAgo\(n\) / daysAgo\(n\) / monthsAgo\(n\) / quartersAgo\(n\) / yearsAgo\(n\) — N-units-ago

Gets a date and time a number of units in the past. The `unitAgo()` methods return the exact moment, the `unitAgoStart()` methods return the start of that period, and the `unitAgoEnd()` methods return the end of it.

The example after the table uses the daysAgo\(\) family. The other families work the same way and differ only in the unit. yearsAgo\(\) has no start or end variant.

All families in this group:

-   minutesAgo\(n\) / minutesAgoStart\(n\) / minutesAgoEnd\(n\)
-   hoursAgo\(n\) / hoursAgoStart\(n\) / hoursAgoEnd\(n\)
-   daysAgo\(n\) / daysAgoStart\(n\) / daysAgoEnd\(n\)
-   monthsAgo\(n\) / monthsAgoStart\(n\) / monthsAgoEnd\(n\)
-   quartersAgo\(n\) / quartersAgoStart\(n\) / quartersAgoEnd\(n\)
-   yearsAgo\(n\)

|Name|Type|Description|
|----|----|-----------|
|n|Number|Number of units in the past, as an integer. Minimum value: 0.|

|Type|Description|
|----|-----------|
|String|Date and time string for the exact moment, the start of the period, or the end of the period, depending on the method.|

This example gets the exact moment three days ago, along with the start and end of that day, and logs all three.

```
mgs.info('Exact: ' + mgs.daysAgo(3));
        mgs.info('Start: ' + mgs.daysAgoStart(3));
        mgs.info('End: ' + mgs.daysAgoEnd(3));
```

Output:

```
Exact: 2026-08-23 16:44:17
        Start: 2026-08-23 00:00:00
        End: 2026-08-23 23:59:59
```

This example counts the active tasks that haven't been updated in the last seven days, such as to flag tasks that need attention.

```
var cutoff = mgs.daysAgo(7);
        var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true^sys_updated_on<' + cutoff);
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('Stale tasks: ' + count);
```

Output:

```
Stale tasks: 3
```

This example gets the exact moment 10 minutes ago, along with the start and end of that minute, and logs all three.

```
mgs.info('Exact: ' + mgs.minutesAgo(10));
        mgs.info('Start: ' + mgs.minutesAgoStart(10));
        mgs.info('End: ' + mgs.minutesAgoEnd(10));
```

Output:

```
Exact: 2026-08-26 16:34:17
        Start: 2026-08-26 16:34:00
        End: 2026-08-26 16:34:59
```

This example gets the exact moment two hours ago, along with the start and end of that hour, and logs all three.

```
mgs.info('Exact: ' + mgs.hoursAgo(2));
        mgs.info('Start: ' + mgs.hoursAgoStart(2));
        mgs.info('End: ' + mgs.hoursAgoEnd(2));
```

Output:

```
Exact: 2026-08-26 14:44:17
        Start: 2026-08-26 14:00:00
        End: 2026-08-26 14:59:59
```

This example gets the exact moment two months ago, along with the start and end of that month, and logs all three.

```
mgs.info('Exact: ' + mgs.monthsAgo(2));
        mgs.info('Start: ' + mgs.monthsAgoStart(2));
        mgs.info('End: ' + mgs.monthsAgoEnd(2));
```

Output:

```
Exact: 2026-06-26 16:44:17
        Start: 2026-06-01 00:00:00
        End: 2026-06-30 23:59:59
```

This example gets the exact moment one quarter ago, along with the start and end of that quarter, and logs all three.

```
mgs.info('Exact: ' + mgs.quartersAgo(1));
        mgs.info('Start: ' + mgs.quartersAgoStart(1));
        mgs.info('End: ' + mgs.quartersAgoEnd(1));
```

Output:

```
Exact: 2026-05-26 16:44:17
        Start: 2026-04-01 00:00:00
        End: 2026-06-30 23:59:59
```

This example counts the active tasks that were created more than one year ago, such as to find old tasks that might need to be closed.

```
var cutoff = mgs.yearsAgo(1);
        var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true^sys_created_on<' + cutoff);
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('Active tasks older than one year: ' + count);
```

Output:

```
Active tasks older than one year: 12
```

## MobileGlideSystem - nil\(Object value\)

Determines whether the value is null, undefined, or an empty string.

|Name|Type|Description|
|----|----|-----------|
|value|Object|Value to test.|

<table id="table_MGS-nil_O_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Returns whether the null, undefined, or an empty string.Possible values:

-   true: Value is null, undefined, or an empty string.
-   false: The value is anything else.

</td></tr></tbody>
</table>This example checks whether the short description of the current record has no value and logs the result.

```
mgs.info(mgs.nil(current.getValue('short_description')));
```

Output:

```
false
```

This example shows an error message when the short description has no value. One check covers a null value, which getValue\(\) returns when the field isn't readable, and an empty string.

```
var description = current.getValue('short_description');
        if (mgs.nil(description)) {
        mgs.addErrorMessage('Enter a short description before you save.');
        }
```

## MobileGlideSystem - now\(\)

Gets the current date, with no time of day. To get the date and time, use nowDateTime\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current date, in the user's date format, such as `MM/dd/yyyy`. The date is based on the platform's internal \(UTC\) time zone, so it can differ from the user's local date late in the day.|

This example gets the current date and logs it.

```
mgs.info(mgs.now());
```

Output:

```
08/26/2026
```

This example builds a title for a daily log. Because now\(\) uses UTC, the date can differ from the user's local date near midnight. Use nowDateTime\(\) when the user's date matters.

```
var title = 'Inspection log for ' + mgs.now();
        mgs.info(title);
```

Output:

```
Inspection log for 08/26/2026
```

## MobileGlideSystem - nowDateTime\(\)

Gets the current date and time in the user's time zone and display format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current date and time in the current user's time zone and display format. Returns the string `NULL` if the value is null. To get only the date, use now\(\). To get the UTC date and time in the internal format, use nowNoTZ\(\).|

This example gets the current date and time in the user's time zone and display format, and logs it.

```
mgs.info(mgs.nowDateTime());
```

Output:

```
2026-08-26 16:44:17
```

This example shows the user the time that a visit started, in the user's own time zone.

```
var message = 'Visit started at ' + mgs.nowDateTime();
        mgs.addInfoMessage(message);
```

Message shown to the user:

```
Visit started at 2026-08-26 16:44:17
```

## MobileGlideSystem - nowGlideDateTime\(\)

Gets a MobileGlideDateTime object for the current date and time. Use the object's methods to read or compare parts of the date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md)|Object for the current date and time. For its available methods, see [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md).|

This example gets the current date and time as an object and logs its value in the internal format.

```
var gdt = mgs.nowGlideDateTime();
        mgs.info(gdt.getValue());
```

Output:

```
2026-08-26 20:44:17
```

This example builds a log label from the current local date and week of the year, such as for a weekly visit log.

```
var gdt = mgs.nowGlideDateTime();
        var label = 'Visit logged for ' + gdt.getLocalDate().getDisplayValue() + ' (week ' + gdt.getWeekOfYearLocalTime() + ')';
        mgs.info(label);
```

Output:

```
Visit logged for 08/26/2026 (week 35)
```

## MobileGlideSystem - nowNoTZ\(\)

Gets the current date and time in UTC, in the internal format, with no time zone conversion.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current UTC date and time, in the format `yyyy-MM-dd HH:mm:ss`.|

This example gets the current UTC date and time and logs it.

```
mgs.info(mgs.nowNoTZ());
```

Output:

```
2026-08-26 20:44:17
```

This example records when work started on a task. Use the internal format, which is in UTC, for values that you store in date-time fields.

```
var gr = new MobileGlideRecord('wm_task');
        if (gr.get(current.getValue('sys_id'))) {
        gr.setValue('work_start', mgs.nowNoTZ());
        gr.update();
        mgs.info('Work started at ' + gr.getValue('work_start'));
        }
```

Output:

```
Work started at 2026-08-26 20:44:17
```

## MobileGlideSystem - yesterday\(\) / lastWeek\(\)

Gets the date and time 24 hours ago \(yesterday\(\)\) or 7 days ago \(lastWeek\(\)\), in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date and time in the format `yyyy-MM-dd HH:mm:ss`, in the platform's internal time zone.|

This example gets the date and time 24 hours ago and 7 days ago, and logs both.

```
mgs.info(mgs.yesterday());
        mgs.info(mgs.lastWeek());
```

Output:

```
2026-08-25 16:44:17
        2026-08-19 16:44:17
```

This example counts the tasks that have been updated in the last 24 hours, such as for a daily activity summary.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('sys_updated_on>' + mgs.yesterday());
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('Tasks updated since yesterday: ' + count);
```

Output:

```
Tasks updated since yesterday: 4
```

This example counts the tasks that were closed in the last seven days, such as for a weekly activity summary.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('closed_at>' + mgs.lastWeek());
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('Tasks closed in the last week: ' + count);
```

Output:

```
Tasks closed in the last week: 9
```

