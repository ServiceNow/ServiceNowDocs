---
title: MobileGlideTime - Scoped
description: The MobileGlideTime API provides the subset of GlideTime available to mobile scripts. It represents the time-of-day portion of a MobileGlideDateTime value.Gets the time of day in a format that you specify, such as HH:mm.Gets the time of day in the current user's display format.Gets the time of day in the user's time zone, in the internal format.Gets the hour of the time of day on a 12-hour clock, in the user's time zone or in UTC.Gets the hour of the time of day on a 24-hour clock, in the user's time zone or in UTC.Gets the minutes of the time of day, in the user's time zone or in UTC.Gets the seconds of the time of day.Gets the time of day in the internal format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileGlideTimeScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideTime - Scoped

The MobileGlideTime API provides the subset of GlideTime available to mobile scripts. It represents the time-of-day portion of a MobileGlideDateTime value.

MobileGlideTime provides the subset of GlideTime that can be evaluated against the local database on a device. It represents the time-of-day portion of a [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md) value, for scripts that control behavior based on the time of day and not the calendar date, such as a script that checks whether the current time falls within business hours.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

This API contains the following capabilities:

-   Formatting times for display: [MobileGlideTime - getByFormat\(String format\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md), [MobileGlideTime - getDisplayValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md)
-   Getting times for storing and comparing: [MobileGlideTime - getValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md), [MobileGlideTime - getDisplayValueInternal\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md)
-   Getting parts of a time: [MobileGlideTime - getHourOfDayLocalTime\(\) / getHourOfDayUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md), [MobileGlideTime - getHourLocalTime\(\) / getHourUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md), [MobileGlideTime - getMinutesLocalTime\(\) / getMinutesUTC\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md), [MobileGlideTime - getSeconds\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideTimeScopedAPI.md)

For guidance on date time input strings with a list of common format conflicts, refer to [Server-side script use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/useful-server-side-scripts.md).

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getTime()` or `getLocalTime()` method of [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md).

## MobileGlideTime - getByFormat\(String format\)

Gets the time of day in a format that you specify, such as `HH:mm`.

|Name|Type|Description|
|----|----|-----------|
|format|String|Time format pattern, such as `HH:mm` or `HH:mm:ss`.|

|Type|Description|
|----|-----------|
|String|Time of day, formatted according to `format`.|

This example gets the current local time of day and logs it in `HH:mm` format.

```
var time = mgs.nowGlideDateTime().getLocalTime();
        mgs.info(time.getByFormat('HH:mm'));
```

Output:

```
16:44
```

This example formats the same time two ways. It shows the user a short time in a message and writes the full time to the log, such as to record a check-in.

```
var time = mgs.nowGlideDateTime().getLocalTime();
        var shortTime = time.getByFormat('HH:mm');
        var fullTime = time.getByFormat('HH:mm:ss');
        mgs.addInfoMessage('Checked in at ' + shortTime);
        mgs.info('Check-in recorded at ' + fullTime);
```

Message shown to the user:

```
Checked in at 16:44
```

Output written to the log:

```
Check-in recorded at 16:44:17
```

## MobileGlideTime - getDisplayValue\(\)

Gets the time of day in the current user's display format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Time of day in the current user's display format, such as `4:44:17 PM`.|

This example gets the current local time of day in the user's display format and logs it.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getDisplayValue());
```

Output:

```
4:44:17 PM
```

This example shows the user the check-in time in their own display format. Use the display value for text that users read. Use getDisplayValueInternal\(\) or getValue\(\) for values that a script compares or stores.

```
var time = mgs.nowGlideDateTime().getLocalTime();
        mgs.addInfoMessage('Check-in time: ' + time.getDisplayValue());
```

Message shown to the user:

```
Check-in time: 4:44:17 PM
```

## MobileGlideTime - getDisplayValueInternal\(\)

Gets the time of day in the user's time zone, in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Time of day in the internal format, `HH:mm:ss`.|

This example gets the current local time of day in the internal format and logs it.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getDisplayValueInternal());
```

Output:

```
16:44:17
```

This example compares the current local time with a 5:00 PM cutoff. A button condition can use this check to show a Close shift button only after the cutoff. The internal format uses a 24-hour clock with leading zeros, so the strings compare correctly regardless of the user's display format.

```
var currentTime = mgs.nowGlideDateTime().getLocalTime().getDisplayValueInternal();
        var pastCutoff = currentTime > '17:00:00';
        mgs.info('Past cutoff: ' + pastCutoff);
```

Output:

```
Past cutoff: false
```

## MobileGlideTime - getHourLocalTime\(\) / getHourUTC\(\)

Gets the hour of the time of day on a 12-hour clock, in the user's time zone or in UTC.

`getHourLocalTime()` returns the hour in the user's local time zone; `getHourUTC()` returns the equivalent hour in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Hour on a 12-hour clock. Range: 0 to 11. A value of 0 represents both 12:00 AM and 12:00 PM.|

This example gets the hour of the current local time on a 12-hour clock and logs it.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getHourLocalTime());
```

Output:

```
4
```

This example builds a readable hour label with AM or PM. The 12-hour value is 0 for both noon and midnight, so the script shows 12 in that case and uses the 24-hour value to tell AM from PM.

```
var time = mgs.nowGlideDateTime().getLocalTime();
        var hour12 = time.getHourLocalTime();
        var displayHour = hour12 === 0 ? 12 : hour12;
        var period = time.getHourOfDayLocalTime() < 12 ? 'AM' : 'PM';
        mgs.info('Local hour: ' + displayHour + ' ' + period);
```

Output:

```
Local hour: 4 PM
```

This example builds a readable hour label in UTC with AM or PM, such as to show users the UTC time of a scheduled job. The 12-hour value is 0 for both noon and midnight, so the script shows 12 in that case and uses the 24-hour value to tell AM from PM.

```
var time = mgs.nowGlideDateTime().getTime();
        var hour12 = time.getHourUTC();
        var displayHour = hour12 === 0 ? 12 : hour12;
        var period = time.getHourOfDayUTC() < 12 ? 'AM' : 'PM';
        mgs.info('UTC hour: ' + displayHour + ' ' + period);
```

Output:

```
UTC hour: 8 PM
```

## MobileGlideTime - getHourOfDayLocalTime\(\) / getHourOfDayUTC\(\)

Gets the hour of the time of day on a 24-hour clock, in the user's time zone or in UTC.

`getHourOfDayLocalTime()` returns the hour in the user's local time zone; `getHourOfDayUTC()` returns the equivalent hour in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Hour on a 24-hour clock. Range: 0 to 23.|

This example gets the hour of the current local time on a 24-hour clock and logs it.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getHourOfDayLocalTime());
```

Output:

```
16
```

This example works out which shift the current local time falls in, such as to label a work log. The day shift runs from 6:00 AM to 2:00 PM, the evening shift from 2:00 PM to 10:00 PM, and the night shift covers the rest.

```
var hour = mgs.nowGlideDateTime().getLocalTime().getHourOfDayLocalTime();
        var shift = 'Night';
        if (hour >= 6 && hour < 14) {
        shift = 'Day';
        } else if (hour >= 14 && hour < 22) {
        shift = 'Evening';
        }
        mgs.info('Current shift: ' + shift);
```

Output:

```
Current shift: Evening
```

This example checks whether the current time falls within a nightly sync window that’s defined in UTC, from 02:00 to 04:00. A button condition can use this check to hide a Sync now button while the nightly sync runs.

```
var hour = mgs.nowGlideDateTime().getTime().getHourOfDayUTC();
        var inSyncWindow = hour >= 2 && hour < 4;
        mgs.info('UTC hour: ' + hour + ', in sync window: ' + inSyncWindow);
```

Output:

```
UTC hour: 20, in sync window: false
```

## MobileGlideTime - getMinutesLocalTime\(\) / getMinutesUTC\(\)

Gets the minutes of the time of day, in the user's time zone or in UTC.

`getMinutesLocalTime()` returns the minutes in the user's local time zone; `getMinutesUTC()` returns the equivalent minutes in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGT-getMinutesLocalTime_getMinutesUTC_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Minutes after the hour.Range: 0 to 59

</td></tr></tbody>
</table>This example gets the minutes of the current local time and logs them.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getMinutesLocalTime());
```

Output:

```
44
```

This example finds the start of the 15-minute appointment slot that the current time falls in, such as for a scheduling form.

```
var minutes = mgs.nowGlideDateTime().getLocalTime().getMinutesLocalTime();
        var slotStart = Math.floor(minutes / 15) * 15;
        mgs.info('Appointment slot starts at minute ' + slotStart);
```

Output:

```
Appointment slot starts at minute 30
```

This example calculates how many minutes remain until the next scheduled sync. Syncs run every 30 minutes, on the hour and half hour in UTC.

```
var minutes = mgs.nowGlideDateTime().getTime().getMinutesUTC();
        var minutesUntilSync = 30 - (minutes % 30);
        mgs.info('Next sync in ' + minutesUntilSync + ' minutes');
```

Output:

```
Next sync in 16 minutes
```

## MobileGlideTime - getSeconds\(\)

Gets the seconds of the time of day.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Seconds after the minute. Range: 0 to 59.|

This example gets the seconds of the current local time and logs them.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getSeconds());
```

Output:

```
17
```

This example converts the current local time to the number of seconds since midnight, such as to compare two times of day to the second.

```
var time = mgs.nowGlideDateTime().getLocalTime();
        var secondsSinceMidnight = time.getHourOfDayLocalTime() * 3600 + time.getMinutesLocalTime() * 60 + time.getSeconds();
        mgs.info('Seconds since midnight: ' + secondsSinceMidnight);
```

Output:

```
Seconds since midnight: 60257
```

## MobileGlideTime - getValue\(\)

Gets the time of day in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Time of day in the internal format, `HH:mm:ss`.|

This example gets the current local time of day in the internal format and logs it.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getValue());
```

Output:

```
16:44:17
```

This example joins the local date and the local time of day, both in the internal format, to build a date and time string for a visit record.

```
var gdt = mgs.nowGlideDateTime();
        var visitTime = gdt.getLocalDate().getValue() + ' ' + gdt.getLocalTime().getValue();
        mgs.info(visitTime);
```

Output:

```
2026-08-26 16:44:17
```

