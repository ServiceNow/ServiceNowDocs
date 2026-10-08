---
title: MobileGlideDateTime - Scoped
description: The MobileGlideDateTime API provides the subset of GlideDateTime available to mobile scripts. It gives a script structured access to a date and time value.Compares this datetime with another.Compares this datetime with another MobileGlideDateTime for equality, or determines whether it occurs after, before, on-or-after, or on-or-before the specified datetime.Gets the date portion, expressed in the system time zone or in the current user's time zone.Gets the day of the month, in the user's time zone or in UTC.Gets the day of the week, in the user's time zone or in UTC.Gets the number of days in the month, in the user's time zone or in UTC.Gets the amount of time, in milliseconds, that daylight saving time is offset.Gets the current error message.Gets the month, in the user's time zone or in UTC.Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.Gets the time portion, or the time portion expressed in the current user's time zone.Gets the time zone offset in milliseconds.Gets the object's time in the local time zone, in the user's display format or in the internal format.Gets the date-time value in the internal format, the current user's display format, and the display value expressed in the internal format, respectively.Gets the number of the week in the year, in the user's time zone or in UTC.Gets the four-digit year, in the user's time zone or in UTC.Determines whether this datetime uses a daylight saving offset.Determines whether the value is a valid date and time.Returns the string representation of the datetime value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileGlideDateTimeScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideDateTime - Scoped

The MobileGlideDateTime API provides the subset of GlideDateTime available to mobile scripts. It gives a script structured access to a date and time value.

MobileGlideDateTime provides the subset of GlideDateTime that can be evaluated against the local database on a device. It gives a script structured access to the components of a date and time value, including the day, month, year, and week, in both local time and UTC, as well as comparison operators. A value can also be split into a[MobileGlideDate - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateScopedAPI.md) and [MobileGlideTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideTimeScopedAPI.md) pair.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public value constructor. Obtain an instance from the `nowGlideDateTime()` method of [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideSystemScopedAPI.md).

## MobileGlideDateTime - compareTo\(MobileGlideDateTime gdt\)

Compares this datetime with another.

|Name|Type|Description|
|----|----|-----------|
|gdt|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md)|The datetime to compare against.|

|Type|Description|
|----|-----------|
|Number|0 if equal, 1 if this datetime is after gdt, -1 if before. Range: -1 to 1.|

This example calls compareTo\_M.

```
mgs.info(mgs.nowGlideDateTime().compareTo(mgs.nowGlideDateTime()));
```

Output:

```
0
```

## MobileGlideDateTime - equals\(\) / after\(\) / before\(\) / onOrAfter\(\) / onOrBefore\(\)

Compares this datetime with another MobileGlideDateTime for equality, or determines whether it occurs after, before, on-or-after, or on-or-before the specified datetime.

|Name|Type|Description|
|----|----|-----------|
|gdt|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md)|The datetime to compare against.|

|Type|Description|
|----|-----------|
|Boolean|Result of the comparison named by the method called.|

This example calls equals\_after\_before\_onOrAfter\_onOrBefore.

```
var dueDate = current.due_date.getValue();
var now = mgs.nowGlideDateTime();
mgs.info(now.after(dueDate));
```

Output:

```
false
```

## MobileGlideDateTime - getDate\(\) / getLocalDate\(\)

Gets the date portion, expressed in the system time zone or in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideDate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateScopedAPI.md)|Date-only portion of this datetime. See [MobileGlideDate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateScopedAPI.md) for its methods.|

This example calls getDate\_getLocalDate.

```
var date = mgs.nowGlideDateTime().getLocalDate();
mgs.info(date.getByFormat('MM/dd/yyyy'));
```

Output:

```
"08/26/2026"
```

## MobileGlideDateTime - getDayOfMonthLocalTime\(\) / getDayOfMonthUTC\(\)

Gets the day of the month, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Day of the month. Range: 1–31.|

This example calls getDayOfMonthLocalTime\_getDayOfMonthUTC.

```
mgs.info(mgs.nowGlideDateTime().getDayOfMonthLocalTime());
```

Output:

```
26
```

## MobileGlideDateTime - getDayOfWeekLocalTime\(\) / getDayOfWeekUTC\(\)

Gets the day of the week, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Day of the week. Range: 1–7 \(Monday = 1\).|

This example calls getDayOfWeekLocalTime\_getDayOfWeekUTC.

```
var isMonday = mgs.nowGlideDateTime().getDayOfWeekLocalTime() === 1;
mgs.info(isMonday);
```

Output:

```
false
```

## MobileGlideDateTime - getDaysInMonthLocalTime\(\) / getDaysInMonthUTC\(\)

Gets the number of days in the month, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of days in the month. Range: 28–31.|

This example calls getDaysInMonthLocalTime\_getDaysInMonthUTC.

```
mgs.info(mgs.nowGlideDateTime().getDaysInMonthLocalTime());
```

Output:

```
31
```

## MobileGlideDateTime - getDSTOffset\(\)

Gets the amount of time, in milliseconds, that daylight saving time is offset.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|DST offset. Unit: milliseconds.|

This example calls getDSTOffset.

```
mgs.info(mgs.nowGlideDateTime().getDSTOffset());
```

Output:

```
0
```

## MobileGlideDateTime - getErrorMsg\(\)

Gets the current error message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current error message. Returns null if there is no error. The backing field is only ever assigned when a real error occurs, such as an unparseable date/time string. It is never set to an empty string.|

This example calls getErrorMsg.

```
mgs.info(mgs.nowGlideDateTime().getErrorMsg());
```

## MobileGlideDateTime - getMonthLocalTime\(\) / getMonthUTC\(\)

Gets the month, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Month number. Range: 1–12.|

This example calls getMonthLocalTime\_getMonthUTC.

```
mgs.info(mgs.nowGlideDateTime().getMonthLocalTime());
```

Output:

```
8
```

## MobileGlideDateTime - getNumericValue\(\)

Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Milliseconds since epoch \(UTC\). Unit: milliseconds.|

This example calls getNumericValue.

```
mgs.info(mgs.nowGlideDateTime().getNumericValue());
```

Output:

```
1787855057000
```

## MobileGlideDateTime - getTime\(\) / getLocalTime\(\)

Gets the time portion, or the time portion expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideTimeScopedAPI.md)|Time-only portion of this datetime. See [MobileGlideTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideTimeScopedAPI.md) for its methods.|

This example calls getTime\_getLocalTime.

```
var time = mgs.nowGlideDateTime().getLocalTime();
mgs.info(time.getHourOfDayLocalTime());
```

Output:

```
16
```

## MobileGlideDateTime - getTZOffset\(\)

Gets the time zone offset in milliseconds.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Time zone offset. Unit: milliseconds.|

This example calls getTZOffset.

```
mgs.info(mgs.nowGlideDateTime().getTZOffset());
```

## MobileGlideDateTime - getUserFormattedLocalTime\(\) / getInternalFormattedLocalTime\(\)

Gets the object's time in the local time zone, in the user's display format or in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Local time in the format named by the method called.|

This example calls getUserFormattedLocalTime\_getInternalFormattedLocalTime.

```
mgs.info(mgs.nowGlideDateTime().getUserFormattedLocalTime());
```

## MobileGlideDateTime - getValue\(\) / getDisplayValue\(\) / getDisplayValueInternal\(\)

Gets the date-time value in the internal format, the current user's display format, and the display value expressed in the internal format, respectively.

`getValue()` returns the internal-format value; `getDisplayValue()` returns the current user's display-format value; `getDisplayValueInternal()` returns the display value expressed in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date-time string in the format described earlier for the method called.|

This example calls getValue\_getDisplayValue\_getDisplayValueInternal.

```
var gdt = mgs.nowGlideDateTime();
mgs.info(gdt.getValue());
```

Output:

```
"2026-08-26 20:44:17"
```

## MobileGlideDateTime - getWeekOfYearLocalTime\(\) / getWeekOfYearUTC\(\)

Gets the number of the week in the year, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Week of the year. Range: 1–53.|

This example calls getWeekOfYearLocalTime\_getWeekOfYearUTC.

```
mgs.info(mgs.nowGlideDateTime().getWeekOfYearLocalTime());
```

Output:

```
35
```

## MobileGlideDateTime - getYearLocalTime\(\) / getYearUTC\(\)

Gets the four-digit year, in the user's time zone or in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Four-digit year.|

This example calls getYearLocalTime\_getYearUTC.

```
mgs.info(mgs.nowGlideDateTime().getYearLocalTime());
```

Output:

```
2026
```

## MobileGlideDateTime - isDST\(\)

Determines whether this datetime uses a daylight saving offset.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether daylight saving is in effect. Possible values: true, daylight saving is in effect; false, daylight saving is not in effect.|

This example calls isDST.

```
mgs.info(mgs.nowGlideDateTime().isDST());
```

Output:

```
false
```

## MobileGlideDateTime - isValid\(\)

Determines whether the value is a valid date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the value is a valid date-time. Possible values: true, this is a valid date-time; false, this is not a valid date-time.|

This example calls isValid.

```
mgs.info(mgs.nowGlideDateTime().isValid());
```

Output:

```
true
```

## MobileGlideDateTime - toString\(\)

Returns the string representation of the datetime value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|String representation of the datetime value.|

This example calls toString.

```
mgs.info(String(mgs.nowGlideDateTime()));
```

