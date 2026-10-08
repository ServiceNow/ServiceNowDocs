---
title: MobileGlideTime - Scoped
description: The MobileGlideTime API provides the subset of GlideTime available to mobile scripts. It represents the time-of-day portion of a MobileGlideDateTime value.Gets the time value in the specified format.Gets the time value in the current user's display format.Gets the display value in the internal format.Gets the hour part of the time on a 12-hour clock, in the user's time zone or in UTC.Gets the hour part of the time on a 24-hour clock, in the user's time zone or in UTC.Gets the minutes, in the user's time zone or in UTC.Gets the seconds.Gets the time value in the internal format and system time zone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileGlideTimeScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideTime - Scoped

The MobileGlideTime API provides the subset of GlideTime available to mobile scripts. It represents the time-of-day portion of a MobileGlideDateTime value.

MobileGlideTime provides the subset of GlideTime that can be evaluated against the local database on a device. It represents the time-of-day portion of a [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md) value, for scripts that control behavior based on the time of day and not the calendar date, such as a script that checks whether the current time falls within business hours.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getTime()` or `getLocalTime()` method of [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md).

## MobileGlideTime - getByFormat\(String format\)

Gets the time value in the specified format.

|Name|Type|Description|
|----|----|-----------|
|format|String|Time format string, for example, "HH:mm".|

|Type|Description|
|----|-----------|
|String|Time value formatted per format.|

This example calls getByFormat\_S.

```
var time = mgs.nowGlideDateTime().getLocalTime();
mgs.info(time.getByFormat('HH:mm'));
```

Output:

```
"16:44"
```

## MobileGlideTime - getDisplayValue\(\)

Gets the time value in the current user's display format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display-format time value.|

This example calls getDisplayValue.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getDisplayValue());
```

Output:

```
"4:44:17 PM"
```

## MobileGlideTime - getDisplayValueInternal\(\)

Gets the display value in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display value expressed in internal format.|

This example calls getDisplayValueInternal.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getDisplayValueInternal());
```

Output:

```
"16:44:17"
```

## MobileGlideTime - getHourLocalTime\(\) / getHourUTC\(\)

Gets the hour part of the time on a 12-hour clock, in the user's time zone or in UTC.

`getHourLocalTime()` returns the hour in the user's local time zone; `getHourUTC()` returns the equivalent hour in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Hour on a 12-hour clock. Range: 0–11 \(0 represents both noon and midnight\).|

This example calls getHourLocalTime\_getHourUTC.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getHourLocalTime());
```

Output:

```
4
```

## MobileGlideTime - getHourOfDayLocalTime\(\) / getHourOfDayUTC\(\)

Gets the hour part of the time on a 24-hour clock, in the user's time zone or in UTC.

`getHourOfDayLocalTime()` returns the hour in the user's local time zone; `getHourOfDayUTC()` returns the equivalent hour in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Hour on a 24-hour clock. Range: 0–23.|

This example calls getHourOfDayLocalTime\_getHourOfDayUTC.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getHourOfDayLocalTime());
```

Output:

```
16
```

## MobileGlideTime - getMinutesLocalTime\(\) / getMinutesUTC\(\)

Gets the minutes, in the user's time zone or in UTC.

`getMinutesLocalTime()` returns the minutes in the user's local time zone; `getMinutesUTC()` returns the equivalent minutes in UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Minutes. Range: 0–59.|

This example calls getMinutesLocalTime\_getMinutesUTC.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getMinutesLocalTime());
```

Output:

```
44
```

## MobileGlideTime - getSeconds\(\)

Gets the seconds.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Seconds. Range: 0–59.|

This example calls getSeconds.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getSeconds());
```

Output:

```
17
```

## MobileGlideTime - getValue\(\)

Gets the time value in the internal format and system time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Internal-format time value.|

This example calls getValue.

```
mgs.info(mgs.nowGlideDateTime().getLocalTime().getValue());
```

Output:

```
"16:44:17"
```

