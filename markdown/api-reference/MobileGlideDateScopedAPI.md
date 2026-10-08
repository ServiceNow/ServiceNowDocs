---
title: MobileGlideDate - Scoped
description: The MobileGlideDate API provides the subset of GlideDate available to mobile scripts. It represents the date-only portion of a MobileGlideDateTime value.Gets the date value in the specified format.Gets the day of the month, not adjusted for time zone.Gets the date value in the current user's display format.Gets the display value in the internal format \(yyyy-MM-dd\).Gets the month, not adjusted for time zone.Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.Gets the date value in the internal format and system time zone.Gets the four-digit year, not adjusted for time zone.Determines whether this value is a valid date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileGlideDateScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideDate - Scoped

The MobileGlideDate API provides the subset of GlideDate available to mobile scripts. It represents the date-only portion of a MobileGlideDateTime value.

MobileGlideDate provides the subset of GlideDate that can be evaluated against the local database on a device. It represents the date-only portion of a [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md) value, for scripts that need only the calendar date, such as a script that checks whether a due date falls on the current date, without accounting for the time of day.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getDate()` or `getLocalDate()` method of [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md).

## MobileGlideDate - getByFormat\(String format\)

Gets the date value in the specified format.

|Name|Type|Description|
|----|----|-----------|
|format|String|Date format string, for example, "MM/dd/yyyy".|

|Type|Description|
|----|-----------|
|String|Date value formatted per format.|

This example calls getByFormat\_S.

```
var dueDate = mgs.nowGlideDateTime().getDate();
mgs.info(dueDate.getByFormat('MM/dd/yyyy'));
```

Output:

```
"08/26/2026"
```

## MobileGlideDate - getDayOfMonthNoTZ\(\)

Gets the day of the month, not adjusted for time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Day of the month. Range: 1–31.|

This example calls getDayOfMonthNoTZ.

```
mgs.info(mgs.nowGlideDateTime().getDate().getDayOfMonthNoTZ());
```

Output:

```
26
```

## MobileGlideDate - getDisplayValue\(\)

Gets the date value in the current user's display format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display-format date value.|

This example calls getDisplayValue.

```
mgs.info(mgs.nowGlideDateTime().getDate().getDisplayValue());
```

Output:

```
"08/26/2026"
```

## MobileGlideDate - getDisplayValueInternal\(\)

Gets the display value in the internal format \(yyyy-MM-dd\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display value expressed in internal format.|

This example calls getDisplayValueInternal.

```
mgs.info(mgs.nowGlideDateTime().getDate().getDisplayValueInternal());
```

Output:

```
"2026-08-26"
```

## MobileGlideDate - getMonthNoTZ\(\)

Gets the month, not adjusted for time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Month number. Range: 1–12.|

This example calls getMonthNoTZ.

```
mgs.info(mgs.nowGlideDateTime().getDate().getMonthNoTZ());
```

Output:

```
8
```

## MobileGlideDate - getNumericValue\(\)

Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Milliseconds since epoch \(UTC\). Unit: milliseconds.|

This example calls getNumericValue.

```
mgs.info(mgs.nowGlideDateTime().getDate().getNumericValue());
```

Output:

```
1787788800000
```

## MobileGlideDate - getValue\(\)

Gets the date value in the internal format and system time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Internal-format date value.|

This example calls getValue.

```
mgs.info(mgs.nowGlideDateTime().getDate().getValue());
```

Output:

```
"2026-08-26"
```

## MobileGlideDate - getYearNoTZ\(\)

Gets the four-digit year, not adjusted for time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Four-digit year.|

This example calls getYearNoTZ.

```
mgs.info(mgs.nowGlideDateTime().getDate().getYearNoTZ());
```

Output:

```
2026
```

## MobileGlideDate - isValid\(\)

Determines whether this value is a valid date.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the value is a valid date. Possible values: true, this is a valid date; false, this is not a valid date.|

This example calls isValid.

```
mgs.info(mgs.nowGlideDateTime().getDate().isValid());
```

Output:

```
true
```

