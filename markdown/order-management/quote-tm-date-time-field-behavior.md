---
title: Date and time field fields
description: Reference for how date and time fields behave in ServiceNow CPQ ServiceNow Quote Experience rules and scripts, including comparison operators, null handling, and supported aggregate functions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-date-time-field-behavior.html
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Fields, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Date and time field fields

Reference for how date and time fields behave in ServiceNow CPQ ServiceNow Quote Experience rules and scripts, including comparison operators, null handling, and supported aggregate functions.

## Date and time fields in quoting

Date and time fields in ServiceNow CPQ serve two primary purposes in a quoting context.

-   **Term calculations**

    Calculate contract terms, start and end dates, renewal dates, and subscription lengths. Blank or null date values can affect term accuracy — use system defaults such as the current date, or flag missing values using error messages in rules.

-   **Audit events**

    Track activities such as quote creation, pricing changes, and approval events. Missing dates indicate incomplete data and should be flagged for review.


## Date and time formats

ServiceNow Quote Experience supports the following date and time formats.

|Format type|Format pattern|Example|
|-----------|--------------|-------|
|Date only|`YYYY-MM-DD`|`2024-11-07`|
|Date and time|`YYYY-MM-DDTHH:MM:SS`|`2024-10-22T14:30:00`|
|UTC \(stored format\)|`YYYY-MM-DDTHH:MM:SSZ`|`2024-10-22T14:30:00Z`|

Date-only fields are time-zone agnostic. All date and time values are stored in Coordinated Universal Time \(UTC\) to avoid time-zone discrepancies. Administrators can choose whether to include the time component when configuring a date/time field.

In the ServiceNow Quote Experience layout, the field type value that controls display behavior is:

-   `"type":"Date"` — displays only the date component.
-   `"type":"DateTime"` — displays both date and time components.

## Null and blank date behavior in scripts

Blank and null date values follow specific comparison rules in ServiceNow Quote Experience scripts and rule conditions.

-   Blank/null dates compare as `false` unless compared directly to another blank value.
-   The default value of a date field is empty \(null\) unless a default is specified in the field configuration.

The following examples show blank date comparison outcomes.

|Expression|Result|Explanation|
|----------|------|-----------|
|`date123 = ""`|`true`|A blank date compared to a blank string evaluates to true.|
|`date123 != ""`|`false`|A blank date compared as not-equal to blank evaluates to false.|

## Supported comparison operators

The following comparison operators are supported for date and time field values in rule conditions and scripts.

|Operator|Behavior|
|--------|--------|
|`<`|Less than. Always evaluates to `false` when either operand is blank or null.|
|`<=`|Less than or equal to. Always evaluates to `false` when either operand is blank or null.|
|`>`|Greater than. Always evaluates to `false` when either operand is blank or null.|
|`>=`|Greater than or equal to. Always evaluates to `false` when either operand is blank or null.|
|`=`|Equal to. Evaluates to `true` only when both operands are blank.|
|`!=`|Not equal to. Evaluates to `false` when either operand is blank or null.|

## Aggregate functions for date fields

The following aggregate functions are supported for date field values. Use these in determination rule scripts to calculate date values across transaction lines.

|Function|Behavior|Notes|
|--------|--------|-----|
|`Max`|Returns the latest date in the set.|Supported.|
|`Min`|Returns the earliest date in the set.|Supported.|
|`Count`|Counts non-empty date values in the set.|Supported.|
|`Sum`|Not applicable to date values.|Not recommended — may trigger compile-time errors.|
|`Avg`|Not applicable to date values.|Not recommended — may trigger compile-time errors.|

## Date calculation script example

The following script calculates the difference between a start date and an end date in months and days, and stores the result in a subscription term field. Use this pattern in a determination rule action to populate a summary field from two date inputs.

```
// Calculates the difference between start and end dates in months and
// days. Stores the result in Subscription Term (Months).

var yearsDiff =
  txn.custom.endDate.getFullYear() - txn.custom.startDate.getFullYear();
var monthsDiff =
  txn.custom.endDate.getMonth() - txn.custom.startDate.getMonth();
var totalMonths = yearsDiff * 12 + monthsDiff;

var startDay = txn.custom.startDate.getDate();
var endDay = txn.custom.endDate.getDate();
var daysInMonth = new Date(
  txn.custom.endDate.getFullYear(),
  txn.custom.endDate.getMonth() + 1,
  0
).getDate();
var dayFraction = (endDay - startDay + 1) / daysInMonth;

totalMonths += dayFraction;
return Math.floor(totalMonths * 1000) / 1000;
```

**Related topics**  


[Quote transaction fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-fields.md)

[Transaction-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-header-level-system-fields.md)

[Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-line-level-system-fields.md)

[Create a transaction field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-field.md)

