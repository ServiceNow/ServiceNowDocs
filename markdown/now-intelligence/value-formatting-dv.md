---
title: Value formatting in data visualizations
description: In most data visualizations, you can configure how numerical values look when you publish the report.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-05-06"
reading_time_minutes: 3
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Value formatting in data visualizations

In most data visualizations, you can configure how numerical values look when you publish the report.

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

    For values greater than one minute, simplifies a number by rounding, while keeping it close to its value. See the next section, Rounding options.

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

**Parent Topic:**[Configure data visualizations](../../performance-analytics/concept/configure-data-visualizations.md)

