---
title: MobileGlideSystem - Scoped
description: The MobileGlideSystem API provides utility methods for the current session, including user information, date and time values, and script logging.Adds an error message for the current session, surfaced to the user in the mobile client.Adds an info message for the current session, surfaced to the user in the mobile client.Gets the UTC start or end date-time of the day containing the given MobileGlideDateTime.Gets the UTC start or end date-time of a fixed named relative range \(a relative month, quarter, year, day, hour, or minute window\).Generates a date-time string for the given date and range.Gets the translated message for the given message ID, substituting positional placeholders in the message text.Gets the MobileGlideUser object for the current user.Gets the display name of the current user.Gets the sys\_id of the current user.Gets the username of the current user.Determines whether the current user has the specified role.Logs an informational message for debugging.Gets a date-time N units in the past — either the exact moment \(unitAgo\(n\)\), or the start \(unitAgoStart\(n\)\) or end \(unitAgoEnd\(n\)\) of that unit's containing period.Determines whether the value is null, undefined, or an empty string.Gets the current date. Despite the generic name, this returns a date only, with no time-of-day component, unlike nowDateTime\(\).Gets the current date and time.Gets a MobileGlideDateTime object with the current date and time.Gets the current date and time in UTC, without time zone conversion.Gets the date and time 24 hours ago, or 7 days ago.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileGlideSystemScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideSystem - Scoped

The MobileGlideSystem API provides utility methods for the current session, including user information, date and time values, and script logging.

MobileGlideSystem methods provide the subset of GlideSystem behavior that can be evaluated against the local database on a device: identity and role checks for the current user, and logging and messaging. Most of the class consists of date-range helpers that mirror the GlideSystem date-range shortcuts used in filters and reports, such as the beginning of the previous quarter. These helpers let a script express a relative time window without calculating dates directly.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API Access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class can't be instantiated. All members are static delegates, and the class is accessed through the variable `mgs`, which the mobile scripting preamble declares as `var mgs = sn_mobile_scripting.MobileGlideSystem;`.

## MobileGlideSystem - addErrorMessage\(String error\)

Adds an error message for the current session, surfaced to the user in the mobile client.

|Name|Type|Description|
|----|----|-----------|
|error|String|Error text to display to the user.|

|Type|Description|
|----|-----------|
|void| |

This example calls addErrorMessage\_S.

```
mgs.addErrorMessage('This field cannot be edited while the record is closed.');
```

## MobileGlideSystem - addInfoMessage\(String message\)

Adds an info message for the current session, surfaced to the user in the mobile client.

|Name|Type|Description|
|----|----|-----------|
|message|String|Text to display to the user.|

|Type|Description|
|----|-----------|
|void| |

This example calls addInfoMessage\_S.

```
mgs.addInfoMessage('Saved locally — will sync when back online.');
```

## MobileGlideSystem - beginningOfDay\(MobileGlideDateTime dateTime\) / endOfDay\(MobileGlideDateTime dateTime\)

Gets the UTC start or end date-time of the day containing the given MobileGlideDateTime.

Unlike the fixed named-range methods, this method takes a [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md) parameter rather than being parameterless.

|Name|Type|Description|
|----|----|-----------|
|dateTime|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md)|The date-time whose containing day's start/end is returned.|

|Type|Description|
|----|-----------|
|String|UTC date-time at the start/end of the day containing dateTime.|

This example calls beginningOfDay\_M\_endOfDay\_M.

```
var dayStart = mgs.beginningOfDay(mgs.nowGlideDateTime());
mgs.info(dayStart);
```

Output:

```
"2026-08-26 00:00:00"
```

## MobileGlideSystem - beginningOfX\(\) / endOfX\(\) — relative date-range shortcuts \(35 pairs, 70 methods\)

Gets the UTC start or end date-time of a fixed named relative range \(a relative month, quarter, year, day, hour, or minute window\).

One full worked example is given following this note; the remaining 34 pairs \(68 methods\) differ only in the named range, not in shape or behavior. Every pair is still listed by name so none is dropped from this documentation set.

**Scope decision \(see source-mapping.md\):** this single reference topic documents the entire 35-pair/70-method family the source attachment \(DOC1138071-mgs.docx\) consolidated under one heading. This deviates from the real GlideSystem corpus convention. That convention gives beginningOfThisMonth\(\) and endOfThisMonth\(\) their own separate reference topic files, for example r\_GS-beginningOfThisMonth.dita and r\_GS-endOfThisMonth.dita. This is flagged for the writer to decide whether MobileGlideSystem should also get one-file-per-method splitting before real promotion.

All 35 beginningOfX\(\)/endOfX\(\) pairs in this family:

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
|String|UTC date-time at the start/end of the named range.|

This example shows the worked pair, beginningOfThisMonth\(\)/endOfThisMonth\(\); every other pair in this family behaves identically.

```
var start = mgs.beginningOfThisMonth();
var end = mgs.endOfThisMonth();
mgs.info(start + ' to ' + end);
```

Output:

```
"2026-08-01 00:00:00 to 2026-08-31 23:59:59"
```

## MobileGlideSystem - dateGenerate\(String date, String range\)

Generates a date-time string for the given date and range.

|Name|Type|Description|
|----|----|-----------|
|date|String|Date in yyyymmdd format, for example, "20260215".|
|range|String|Either 'start' \(00:00:00\), 'end' \(23:59:59\), or a specific hh:mm:ss \(24hr\) time.|

|Type|Description|
|----|-----------|
|String|Date-time string in the instance's date format.|

This example calls dateGenerate\_S\_S.

```
var rangeStart = mgs.dateGenerate('20260215', 'start');
mgs.info(rangeStart);
```

Output:

```
"2026-02-15 00:00:00"
```

## MobileGlideSystem - getMessage\(String messageId, Object args\)

Gets the translated message for the given message ID, substituting positional placeholders in the message text.

|Name|Type|Description|
|----|----|-----------|
|messageId|String|Key of a sys\_ui\_message record. If no record matches, the platform falls back to returning messageId itself as the message text.|
|args|Object|Optional. A single value, or an array of values, substituted positionally for \{0\}, \{1\}, and so on, placeholders in the message text.|

|Type|Description|
|----|-----------|
|String|Translated message text with substitutions applied.|

This example calls getMessage\_S\_O.

```
mgs.info(mgs.getMessage('This {0} record is currently locked.', ['incident']));
```

Output:

```
"This incident record is currently locked."
```

## MobileGlideSystem - getUser\(\)

Gets the MobileGlideUser object for the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideUser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideUserScopedAPI.md)|The current user. For the available methods, see [MobileGlideUser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideUserScopedAPI.md).|

This example gets the display name of the current user and writes it to the log.

```
var displayName = mgs.getUser().getDisplayName();
        mgs.info(displayName);
```

Output:

```
Jordan Alvarez
```

## MobileGlideSystem - getUserDisplayName\(\)

Gets the display name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's display name.|

This example calls getUserDisplayName.

```
mgs.info(mgs.getUserDisplayName());
```

Output:

```
"Jordan Alvarez"
```

## MobileGlideSystem - getUserID\(\)

Gets the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current user. Maximum length: 32.|

This example calls getUserID.

```
mgs.info(mgs.getUserID());
```

Output:

```
"62826bf03710200044e0bfc8bcbe5dec"
```

## MobileGlideSystem - getUserName\(\)

Gets the username of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's login name.|

This example calls getUserName.

```
mgs.info(mgs.getUserName());
```

Output:

```
"employee.smith"
```

## MobileGlideSystem - hasRole\(String role\)

Determines whether the current user has the specified role.

|Name|Type|Description|
|----|----|-----------|
|role|String|Name of the role to check, for example, 'itil'.|

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the current user has the specified role. Possible values: true, user has the role; false, user does not have the role.|

This example calls hasRole\_S.

```
if (mgs.hasRole('itil')) {
  mgs.info('User is ITIL');
}
```

Output:

```
"User is ITIL"
```

## MobileGlideSystem - info\(String message\)

Logs an informational message for debugging.

|Name|Type|Description|
|----|----|-----------|
|message|String|Text to write to the system log.|

|Type|Description|
|----|-----------|
|void| |

This example writes the sys\_id of the current record to the log as part of a condition script.

```
mgs.info('Condition evaluated for record ' + current.getValue('sys_id'));
```

## MobileGlideSystem - minutesAgo\(n\) / hoursAgo\(n\) / daysAgo\(n\) / monthsAgo\(n\) / quartersAgo\(n\) / yearsAgo\(n\) — N-units-ago shortcuts \(6 families, 18 methods\)

Gets a date-time N units in the past — either the exact moment \(unitAgo\(n\)\), or the start \(unitAgoStart\(n\)\) or end \(unitAgoEnd\(n\)\) of that unit's containing period.

One full worked example is given following this note; the other families differ only in the unit \(minutes, hours, days, months, quarters, years\), not in shape or behavior. Every family is confirmed exposed on mgs by its own static function bindings in the runtime implementation.

**Scope decision \(see source-mapping.md\):** this single reference topic documents the entire 6-family/18-method group the source attachment consolidated under one heading. This is the same documented deviation from the strict one-file-per-method corpus convention as the beginningOfX\(\)/endOfX\(\) family earlier in this class. yearsAgo\(n\) is the one family confirmed with no Start/End variant.

All 6 families in this group:

-   minutesAgo\(n\) / minutesAgoStart\(n\) / minutesAgoEnd\(n\)
-   hoursAgo\(n\) / hoursAgoStart\(n\) / hoursAgoEnd\(n\)
-   daysAgo\(n\) / daysAgoStart\(n\) / daysAgoEnd\(n\)
-   monthsAgo\(n\) / monthsAgoStart\(n\) / monthsAgoEnd\(n\)
-   quartersAgo\(n\) / quartersAgoStart\(n\) / quartersAgoEnd\(n\)
-   yearsAgo\(n\)

|Name|Type|Description|
|----|----|-----------|
|n|Number|How many units in the past. Integer. Minimum value: 0.|

|Type|Description|
|----|-----------|
|String|Date-time string per the method's semantics \(exact / period start / period end\).|

This example shows the worked family, daysAgo\(n\)/daysAgoStart\(n\)/daysAgoEnd\(n\); every other family in this group behaves identically, parameterized by its own unit.

```
var threeDaysAgo = mgs.daysAgo(3);
var thatDayStart = mgs.daysAgoStart(3);
var thatDayEnd = mgs.daysAgoEnd(3);
mgs.info(threeDaysAgo);
```

Output:

```
"2026-08-23 16:44:17"
```

## MobileGlideSystem - nil\(Object value\)

Determines whether the value is null, undefined, or an empty string.

|Name|Type|Description|
|----|----|-----------|
|value|Object|Value to test.|

|Type|Description|
|----|-----------|
|Boolean|true if value is null, undefined, or an empty string; false otherwise.|

This example calls nil\_O.

```
mgs.info(mgs.nil(current.getValue('short_description')));
```

Output:

```
false
```

## MobileGlideSystem - now\(\)

Gets the current date. Despite the generic name, this returns a date only, with no time-of-day component, unlike nowDateTime\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current date only \(no time-of-day\), in the user's preferred date pattern \(for example, MM/dd/yyyy\) computed in the platform's internal time zone.|

This example calls now.

```
mgs.info(mgs.now());
```

Output:

```
"08/26/2026"
```

## MobileGlideSystem - nowDateTime\(\)

Gets the current date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current date and time, in the current user's display format and actual session time zone. Falls back to the literal string "NULL" if the underlying value is somehow null. This is distinct from now\(\), which returns a date only, computed in the platform's internal/UTC time zone rather than the user's. It is also distinct from nowNoTZ\(\), which returns date and time in the fixed internal format and that same internal/UTC time zone.|

This example calls nowDateTime.

```
mgs.info(mgs.nowDateTime());
```

Output:

```
"2026-08-26 16:44:17"
```

## MobileGlideSystem - nowGlideDateTime\(\)

Gets a MobileGlideDateTime object with the current date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md)|Current date-time object. See [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md) for its methods.|

This example calls nowGlideDateTime.

```
var gdt = mgs.nowGlideDateTime();
mgs.info(gdt.getValue());
```

Output:

```
"2026-08-26 20:44:17"
```

## MobileGlideSystem - nowNoTZ\(\)

Gets the current date and time in UTC, without time zone conversion.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Current UTC date-time, format yyyy-mm-dd hh:mm:ss.|

This example calls nowNoTZ.

```
mgs.info(mgs.nowNoTZ());
```

Output:

```
"2026-08-26 20:44:17"
```

## MobileGlideSystem - yesterday\(\) / lastWeek\(\)

Gets the date and time 24 hours ago, or 7 days ago.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date-time in the fixed internal format \(yyyy-MM-dd HH:mm:ss\) and the platform's internal/UTC time zone.|

This example calls yesterday\_lastWeek.

```
mgs.info(mgs.yesterday());
mgs.info(mgs.lastWeek());
```

Output:

```
"2026-08-25 16:44:17"
"2026-08-19 16:44:17"
```

