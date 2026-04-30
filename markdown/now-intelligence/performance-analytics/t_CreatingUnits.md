---
title: Create a unit
description: You can define units in which Performance Analytics indicator scores are shown. Units can be numbers, percentages, currencies, quantities of time, or any other entity you define. The most commonly used units are provided by default.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a unit

You can define units in which Performance Analytics indicator scores are shown. Units can be numbers, percentages, currencies, quantities of time, or any other entity you define. The most commonly used units are provided by default.

## Before you begin

Roles required: pa\_power\_user \(without navigation\), pa\_data\_collector, pa\_admin, or admin

**Important:** Do not delete any of the units that are provided by default. For example, if you remove the **Use reference currency** unit, it is not possible to show indicator scores in a reference currency.

## Procedure

1.  Navigate to **All** and search for `pa_units_list.do` in the **Filter** field.

    This approach works for all permitted roles regardless of Platform Analytics migration status.

2.  Select **New**.

3.  Enter the **Name** of the unit.

    For example, `Gallon`.

4.  Specify the way the unit must be formatted.

    For example, \{0\}Gal gives you the number of gallons with the abbreviation Gal. For currencies, you can place the symbol for the unit in front of the number, such as $\{0\}.

5.  Click **Submit**.

    Units can be used for automated, manual, and formula indicators.


