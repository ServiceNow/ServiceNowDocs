---
title: Value formatting in reports
description: In most reports, you can configure how numerical values look when you publish the report.In existing reports, you can configure formatted values on the Configure tab of the Report Designer.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Value formatting in reports

In most reports, you can configure how numerical values look when you publish the report.

## Supported value formats

A limited number of visualization types support value formatting.

|Visualization type|Supported value formats|
|------------------|-----------------------|
|Single score|Both number and duration formatting|
|Multilevel pivot|Both number and duration formatting|
|Horizontal and vertical bar|Only duration formatting|
|Pie|Only duration formatting|
|Time series visualizations \(Area, column, line, spline, and step line\)|Only duration formatting|
|Geomap|Only duration formatting|

Formatting applies for aggregate values.

## Types of value formatting

-   **Unit format**

    Show the format of time fields as d/h/m/s or day/hour/minute/second.

-   **Maximum/Minimum duration unit**

    Select the largest or smallest unit to be shown: Day, Hour, Minute, or Second.

-   **Hide seconds when unit is greater than one minute**

    Removes seconds display when a duration value is greater than one minute. Only available if you choose **Second** as the minimum duration unit.

-   **Decimal precision**

    Number of decimal places to show, from zero to four decimal places.

    **Note:** Decimal precision is not supported on currency fields.

-   **Rounding**

    For values greater than one minute, simplifies a number by rounding, while keeping it close to its value. See [Rounding options](value-formatting-reports.md#section_pb5_v5n_nnb).

-   **Use the thousands group separator**

    Separate a value of thousands or higher with a comma or period.

-   **Enable abbreviation**

    Show a value of thousands or higher with a single character.

    **Note:** Abbreviation for Currency, Price, or FX Currency values is not supported.

-   **Hide value in tooltip**

    Do not show the unrounded, unabbreviated value in the tooltip.


## Rounding options

For values greater than one minute, rounding options simplify a number, but keep it close to its value. Select from these rounding options:

-   Up - to the next larger whole number if positive and to the next smaller whole number if negative. Example: For original values of:
    -   1.1 returns a value of 2
    -   1.6 returns a value of 2
    -   -1.6 returns a value of -2
-   Down - to the next smaller whole number if positive and to the next larger whole number if negative. Example: For original values of:
    -   1.1 returns a value of 1
    -   1.6 returns a value of 1
    -   -1.6 returns a value of -1
-   Ceiling - to the next larger whole number, toward the positive. Example: For original values of:
    -   1.1 returns a value of 2
    -   1.6 returns a value of 2
    -   -1.6 returns a value of -1
-   Floor - to the next smaller whole number, toward the negative. Example: For original values of:
    -   1.1 returns a value of 1
    -   1.6 returns a value of 1
    -   -1.6 returns a value of -2
-   Half up - to the nearest neighboring whole number. If both neighbors are equidistant, rounds to the next larger whole number. Example: For original values of:
    -   1.1 returns a value of 1
    -   1.6 returns a value of 2
    -   2.5 returns a value of 3
-   Half down - to the nearest neighboring whole number. If both neighbors are equidistant, rounds to the next smaller whole number. Example: For original values of:
    -   1.1 returns a value of 1
    -   1.6 returns a value of 2
    -   2.5 returns a value of 2
-   Half even - to the nearest whole number. If both neighbors are equidistant, rounds to the closest even number. Example: For original values of:
    -   1.1 returns a value of 1
    -   1.6 returns a value of 2
    -   -2.5 returns a value of -2

Summary of rounding options:

|Input number|Up|Down|Ceiling|Floor|Half up|Half down|Half even|
|------------|---|----|-------|-----|-------|---------|---------|
|5.5|6|5|6|5|6|5|6|
|2.5|3|2|3|2|3|2|2|
|1.6|2|1|2|1|2|2|2|
|1.1|2|1|2|1|1|1|1|
|1.0|1|1|1|1|1|1|1|
|-1.0|-1|-1|-1|-1|-1|-1|-1|
|-1.1|-2|-1|-1|-2|-1|-1|-1|
|-1.6|-2|-1|-1|-2|-2|-2|-2|
|-2.5|-3|-2|-2|-3|-3|-2|-2|
|-5.5|-6|-5|-5|-6|-6|-5|-6|

**Parent Topic:**[Advanced Core UI reporting topics](../concept/c_AdvancedReporting.md)

## Configure formatted values in reports

In existing reports, you can configure formatted values on the **Configure** tab of the Report Designer.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report with the values you want to format.

3.  Select the **Configure** tab.

4.  Click Set Value Formatting.

5.  In the Value Formatting window, configure duration, decimal precision, rounding options, unit separators, and abbreviations.

    Value formatting options for a single score report with Count aggregation:

    ![Value formatting example](../image/value-formatting-example.png)


