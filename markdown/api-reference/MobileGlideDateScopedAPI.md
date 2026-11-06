---
title: MobileGlideDate - Scoped
description: The MobileGlideDate API provides methods for working with date-only values \(year, month, and day, with no time of day\) in mobile scripts. This includes formatting a date for display, reading individual date parts, or comparing dates.Gets the date value formatted with a date format pattern that you specify, such as MM/dd/yyyy or MMM d, yyyy.Gets the day of the month from the date value as a number, without converting the date to the user’s or system time zone.Gets the date value formatted in the current user’s date display format. Use this method for dates that users read, such as dates in messages or labels.Gets the date value in the internal date format, yyyy-MM-dd, regardless of the current user’s date format preference.Gets the month from the date value as a number, without converting the date to the user’s or system time zone.Gets the date value as the number of milliseconds since January 1, 1970, 00:00:00 GMT. Use this method to compare, sort, or calculate the time between dates.Gets the date value in the internal date format, yyyy-MM-dd, in the system time zone. Use this method for dates that you store or compare.Gets the four-digit year from the date value, without converting the date to the user’s or system time zone.Determines whether the MobileGlideDate object contains a valid date. Use this method to check a date before you format or compare it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileGlideDateScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideDate - Scoped

The MobileGlideDate API provides methods for working with date-only values \(year, month, and day, with no time of day\) in mobile scripts. This includes formatting a date for display, reading individual date parts, or comparing dates.

MobileGlideDate provides the subset of GlideDate that can be evaluated against the local database on a device. It represents the date-only portion of a [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md) value, for scripts that need only the calendar date, such as a script that checks whether a due date falls on the current date, without accounting for the time of day.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

This API contains the following capabilities:

-   Formatting dates for display: [MobileGlideDate - getByFormat\(String format\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md), [MobileGlideDate - getDisplayValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md)
-   Getting dates for storing and comparing: [MobileGlideDate - getValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md), [MobileGlideDate - getDisplayValueInternal\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md), [MobileGlideDate - getNumericValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md)
-   Getting parts of a date: [MobileGlideDate - getDayOfMonthNoTZ\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md), [MobileGlideDate - getMonthNoTZ\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md), [MobileGlideDate - getYearNoTZ\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md)
-   Validating dates: [MobileGlideDate - isValid\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateScopedAPI.md)

For guidance on date time input strings with a list of common format conflicts, refer to [Server-side script use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/scripts/useful-server-side-scripts.md).

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getDate()` or `getLocalDate()` method of [MobileGlideDateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideDateTimeScopedAPI.md).

## MobileGlideDate - getByFormat\(String format\)

Gets the date value formatted with a date format pattern that you specify, such as MM/dd/yyyy or MMM d, yyyy.

<table id="table_MGD-getByFormat_S_p" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

format

</td><td>

String

</td><td>

Date format pattern to apply to the date value. Use standard date pattern letters, such as yyyy for the four-digit year, MM for the two-digit month, MMM for the abbreviated month name, and dd for the two-digit day.Example: `"MM/dd/yyyy"`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Date value formatted with the specified pattern, such as 08/26/2026 for the pattern MM/dd/yyyy.|

This example gets the current date and logs it in `MM/dd/yyyy` format.

```
var dueDate = mgs.nowGlideDateTime().getDate();
mgs.info(dueDate.getByFormat('MM/dd/yyyy'));
```

Output:

```
"08/26/2026"
```

This example formats the current date as a readable label, such as text that a write-back action adds to a record’s notes.

```
var today = mgs.nowGlideDateTime().getDate();
var label = 'Visit completed on ' + today.getByFormat('MMM d, yyyy');
mgs.info(label);
```

Output:

```
Visit completed on Aug 26, 2026
```

## MobileGlideDate - getDayOfMonthNoTZ\(\)

Gets the day of the month from the date value as a number, without converting the date to the user’s or system time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGD-getDayOfMonthNoTZ_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Day of the month for the date value, such as 26 for August 26.Range: 1-31

</td></tr></tbody>
</table>This example gets the current date and logs the day of the month as a number, without adjusting for time zone.

```
mgs.info(mgs.nowGlideDateTime().getDate().getDayOfMonthNoTZ());
```

Output:

```
26
```

This example checks whether the current date falls within the first five days of the month. A button condition can use this check to show a Submit monthly time sheet button only during the submission window.

```
var day = mgs.nowGlideDateTime().getDate().getDayOfMonthNoTZ();
var inSubmissionWindow = day <= 5;
mgs.info('Day ' + day + ', submission window open: ' + inSubmissionWindow);
```

Output:

```
Day 26, submission window open: false
```

## MobileGlideDate - getDisplayValue\(\)

Gets the date value formatted in the current user’s date display format. Use this method for dates that users read, such as dates in messages or labels.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date value in the current user’s date display format, such as 08/26/2026 for a user whose format is MM/dd/yyyy. The format varies by user, so don’t use this value to store or compare dates.|

This example gets the current date and logs it in the current user’s date display format.

```
mgs.info(mgs.nowGlideDateTime().getDate().getDisplayValue());
```

Output:

```
"08/26/2026"
```

This example builds a confirmation message that shows the date in the current user’s date format. Use the display value for text that users read, and use getValue\(\) for values that you store or compare.

```
var today = mgs.nowGlideDateTime().getDate();
mgs.info('Scheduled for ' + today.getDisplayValue());
```

Output:

```
Scheduled for 08/26/2026
```

## MobileGlideDate - getDisplayValueInternal\(\)

Gets the date value in the internal date format, yyyy-MM-dd, regardless of the current user’s date format preference.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date value in the yyyy-MM-dd format, such as 2026-08-26. The format is the same for every user.|

This example gets the current date and logs it in the internal format, `yyyy-MM-dd`.

```
mgs.info(mgs.nowGlideDateTime().getDate().getDisplayValueInternal());
```

Output:

```
"2026-08-26"
```

This example builds a reference string in `yyyy-MM-dd` format, which stays the same regardless of the user’s date format preference.

```
var today = mgs.nowGlideDateTime().getDate();
        var inspectionRef = 'INSP-' + today.getDisplayValueInternal();
        mgs.info(inspectionRef);
```

Output:

```
INSP-2026-08-26
```

## MobileGlideDate - getMonthNoTZ\(\)

Gets the month from the date value as a number, without converting the date to the user’s or system time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGD-getMonthNoTZ_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Month of the date value, where 1 is January and 12 is December.Range: 1–12

</td></tr></tbody>
</table>This example gets the current date and logs the month as a number from 1 to 12, without adjusting for time zone.

```
mgs.info(mgs.nowGlideDateTime().getDate().getMonthNoTZ());
```

Output:

```
8
```

This example works out the current quarter and checks whether the current month is the first month of that quarter. A button condition can use this check to show a Start quarterly inspection button only at the start of each quarter.

```
var month = mgs.nowGlideDateTime().getDate().getMonthNoTZ();
        var quarter = Math.ceil(month / 3);
        var isFirstMonthOfQuarter = (month % 3 === 1);
        mgs.info('Q' + quarter + ', first month of quarter: ' + isFirstMonthOfQuarter);
```

Output:

```
Q3, first month of quarter: false
```

## MobileGlideDate - getNumericValue\(\)

Gets the date value as the number of milliseconds since January 1, 1970, 00:00:00 GMT. Use this method to compare, sort, or calculate the time between dates.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGD-getNumericValue_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of milliseconds between January 1, 1970, 00:00:00 GMT and the start of the date value.Unit: Milliseconds

</td></tr></tbody>
</table>This example gets the current date and logs it as the number of milliseconds since January 1, 1970, 00:00:00 GMT.

```
mgs.info(mgs.nowGlideDateTime().getDate().getNumericValue());
```

Output:

```
1787788800000
```

## MobileGlideDate - getValue\(\)

Gets the date value in the internal date format, yyyy-MM-dd, in the system time zone. Use this method for dates that you store or compare.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date value in the yyyy-MM-dd format, such as 2026-08-26. The format doesn’t change with the user’s date format preference, so you can use it to store dates or compare them.|

This example gets the current date and logs it in the internal format, `yyyy-MM-dd`, in the system time zone.

```
mgs.info(mgs.nowGlideDateTime().getDate().getValue());
```

Output:

```
"2026-08-26"
```

This example checks whether the current date is a blackout date. A button condition can use this check to hide a Schedule visit button on company holidays. Compare values in internal format because display formats vary by user.

```
var blackoutDates = ['2026-11-26', '2026-12-25'];
        var today = mgs.nowGlideDateTime().getDate().getValue();
        var isBlackout = blackoutDates.indexOf(today) !== -1;
        mgs.info('Today is a blackout date: ' + isBlackout);
```

Output:

```
Today is a blackout date: false
```

## MobileGlideDate - getYearNoTZ\(\)

Gets the four-digit year from the date value, without converting the date to the user’s or system time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Four-digit year of the date value, such as 2026.|

This example gets the current date and logs the four-digit year, without adjusting for time zone.

```
mgs.info(mgs.nowGlideDateTime().getDate().getYearNoTZ());
```

Output:

```
2026
```

This example works out the fiscal year for an organization whose fiscal year starts in July. A write-back action can use the result to set a fiscal year field.

```
var date = mgs.nowGlideDateTime().getDate();
        var year = date.getYearNoTZ();
        var fiscalYear = date.getMonthNoTZ() >= 7 ? year + 1 : year;
        mgs.info('FY' + fiscalYear);
```

Output:

```
FY2027
```

## MobileGlideDate - isValid\(\)

Determines whether the MobileGlideDate object contains a valid date. Use this method to check a date before you format or compare it.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGD-isValid_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the object contains a valid date.Possible values:

-   true: This is a valid date.
-   false: The object is empty or is not a valid date.

</td></tr></tbody>
</table>This example gets the current date and logs whether it is a valid date.

```
mgs.info(mgs.nowGlideDateTime().getDate().isValid());
```

Output:

```
true
```

This example checks that a date is valid before the script formats it. Use this check when the date comes from a record field that might be empty or malformed.

```
var date = mgs.nowGlideDateTime().getDate();
        if (date.isValid()) {
        mgs.info('Scheduled for ' + date.getDisplayValue());
        } else {
        mgs.info('No valid date. Skipping.');
        }
```

Output:

```
Scheduled for 08/26/2026
```

