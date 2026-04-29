---
title: Create a Data snapshots formula indicator
description: Create a formula indicator to calculate a score from two or more Data snapshots indicators.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a Data snapshots formula indicator

Create a formula indicator to calculate a score from two or more Data snapshots indicators.

## Before you begin

Determine whether your use case meets the following requirements:

-   Your license enables you to create indicators.
-   You have Data snapshots enabled on your instance. For more information, see [Activate Data snapshots](activate-unlimited-breakdowns.md#).
-   You have suitable Data snapshots automated indicators.

Role required: pa\_power\_user, pa\_admin, or admin

## About this task

Formulas are often used to:

-   Calculate ratios and percentages.
-   Combine data from different applications.
-   Build predictive indicators based on historic performance.

The fields of a formula indicator are similar to the fields of an automated indicator. However, instead of specifying a Source, you specify a formula. Formulas consist of other indicators, constants, variables, and time series, or any combination of these elements.

**Note:**

-   You must have a subscription for Performance Analytics to create indicators.
-   If you’re using domain separation, the indicator is created in the domain that you’re currently in.

## Procedure

1.  Select the correct application scope.

    The indicator you create will be in the application scope of your session. This application scope must match the application scope of the automated Data snapshots indicators you’ll choose.

2.  Follow one of these procedures to start creating a Data snapshots automated indicator:

    -   Create an indicator from the Indicator library, as described in [Create an indicator from the library](create-indicator-from-library.md).
    -   Navigate to **All** &gt; **Data Snapshots** &gt; **Indicators** &gt; **Formula Indicators - Data Snapshots** and select **New**.
3.  If you selected **Create indicator** from the indicator library, select the Formula indicator type and Data snapshots source type.

    ![Create new indicator page opened from indicator library.](../image/create-ds-form-indicator.png)

4.  In the **Name** field, give the indicator a descriptive name, such as `& incidents completed in time`.

5.  Select the calendar.

    Confirm that the calendar you select supports the frequency of the Data snapshots sources for the indicators in the formula. For example, if you select Industrial Connected Workforce \(ICW\) indicators with the All Activity frequency, you can select the Industrial shift calendar. If you select ICW indicators with the Daily frequency, you can select only the Standard calendar.

6.  Select a calendar frequency.

    Available calendar frequencies depend on the calendar.

7.  Complete the other fields.

    |Field|Description|
    |-----|-----------|
    |Direction|The direction in which you want scores to change. This selection affects Targets and helps you evaluate progress. Set a Direction whenever it makes sense to do so. A Direction is more likely to make sense when applied to cumulative changes than when a Trend by field is specified.|
    |Unit \(optional\)|The unit in which indicator scores are expressed, such as percentage \(%\) or currency \($, €, and so on\)|
    |Show 0 for null value indicators|If the score of a contributing indicator is a null value, such as happens when you divide by zero, the formula result is set to zero.|

8.  Define the Formula for this indicator.

    1.  To put the score of an indicator in the formula, select the **Browse for an indicator** link and select an automated Data Snapshots indicator.

    2.  Add mathematical operators and symbols to the **Formula** as needed.

        Enter any operators or numbers to include in the formula. Use valid operator symbols, such as +, -, /, %, &gt;, &lt;. You can also add more indicators to the formula. For example, to calculate the average age of open incidents, use the following formula: `[[Summed age of open incidents]] / [[Open incidents]] / 24`

    **Note:** Data snapshots indicators don’t support the PAFormulaUtils API. Thus, those methods aren’t available in formulas. Data snapshots indicators also don’t support breakdowns as such. Instead, you can use any fields common to the sources of all the contributing indicators to filter the formula indicator scores on a data visualization or in KPI Details.

9.  In the **Access control** tab, set whether to save this indicator to the library and whether to limit the visibility of the indicator by user, group, or role.

10. Select **Submit** or **Update**.


**Parent Topic:**[Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md)

