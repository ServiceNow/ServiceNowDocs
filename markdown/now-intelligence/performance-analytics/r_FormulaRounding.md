---
title: Rounding and precision in indicators
description: Indicators round fractional results using "Banker's rounding" or mathematical rounding depending on the indicator Precision.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Rounding and precision in indicators

Indicators round fractional results using "Banker's rounding" or mathematical rounding depending on the indicator **Precision**.

## Scores below 10,000

When an indicator has a **Precision** of 0, the indicator rounds the result to the nearest even, whole number. For example, if an indicator with **Precision** 0 calculates the values 7 + \(5 / 2\), the indicator rounds the result up to 10. However, if the formula calculates 2 + \(5 / 2\), the indicator rounds the result down to 4.

When an indicator has a **Precision** greater than 0, the indicator rounds to the nearest decimal point for the given precision. For example, an indicator with **Precision** 1 rounds a result of 4.45 as 4.5.

## Scores above 10,000

For indicator scores above 10,000, the score is rounded off and displayed with unit abbreviations as follows:

|Number|Abbreviation|Example, precision=0|Example, precision=1|
|------|------------|--------------------|--------------------|
|10,000-999,999|Nearest thousand, k|13,291 displayed as 13 k|13,291 displayed as 13.3 k|
|1,000,000-999,999,999|Nearest million, M|17,824,391 displayed as 18 M|17,824,391 displayed as 17.8 M|
|1,000,000,000|Nearest billion, G|2,378,425,321 displayed as 2 G|2,378,425,321 displayed as 2.4 G|
|1,000,000,000,000|Nearest trillion, T|3,456,398,231,094 displayed as 3 T|3,456,398,231,094 displayed as 3.5 T|
|1,000,000,000,000,000|Nearest quadrillion, P \(for Peta\)|18,103,456,398,231,094 displayed as 18 P|18,103,456,398,231,094 displayed as 18.1 P|
|1,000,000,000,000,000,000+|Nearest quintillion, E \(for Exa\)|7,618,103,456,398,231,094 displayed as 8 E|7,618,103,456,398,231,094 displayed as 7.6 E|

**Note:**

-   Unlike numbers under 10,000, large numbers are not rounded off to the nearest even number when precision=0.
-   Unit abbreviations are not configurable.

## Exceptions

Y-axis values plotted on a line or column chart are not rounded. The score and tooltip displayed when you point to a value on the chart are rounded based on the indicator **Precision**.

**Note:** In formula indicators, rounding applies only to the formula result. Values within the formula are not rounded.

