---
title: Create a formula indicator
description: Create a formula indicator to produce a new computed score from one or more other indicators. Besides indicator scores, the formula can include calculations such as the gap between an indicator score and the indicator target.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Formula indicators, Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a formula indicator

Create a formula indicator to produce a new computed score from one or more other indicators. Besides indicator scores, the formula can include calculations such as the gap between an indicator score and the indicator target.

## Before you begin

Role required: pa\_power\_user, pa\_admin, or admin

## About this task

Formulas are often used to:

-   Calculate ratios and percentages.
-   Combine data from different applications.
-   Build predictive indicators based on historic performance.

The fields of a formula indicator are similar to the fields of an automated indicator. However, instead of Source, Additional Conditions, and Collection properties, a Formula Statement is defined. Formulas can consist of other indicators, constants, variables, and time series, or any combination of these elements.

**Note:**

-   You must have a subscription for Performance Analytics to create indicators.
-   If you are using domain separation, the indicator is created in the domain that you are currently in.

## Procedure

1.  Use one of the following navigation paths:

    -   If you are on an upgraded instance that has not migrated to Platform Analytics, navigate to **All** &gt; **Performance Analytics** &gt; **Indicators** &gt; **Formula Indicators** and select **New**.
    -   If you are on a new instance or have migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Indicators** &gt; **Formula Indicators** and select **New**.
2.  In the **Name** field, give the indicator a descriptive name, such as Average duration of open incidents.

3.  In the **Calendars** field, select either the standard calendar or a business or fiscal calendar group.

4.  If you selected a business or fiscal calendar, select the calendar frequency.

    At least one indicator in the formula must match the specified calendar frequency. The choice of calendar frequencies depends on the setting of the business calendar entries or fiscal calendar schedules.

    For example, the Gregorian calendar has Quarter, Month, Week, and Year frequencies. If you are using the Gregorian calendar, you must choose one of these frequencies.

5.  If you prefer that the score of this indicator increases or decreases over time, select **Maximize** or **Minimize** in the **Direction** field.

    Analytical tools and graphic displays use this **Direction** with this indicator.

    **Tip:** Set a direction whenever you can. All key indicators should be set to Maximize or Minimize.

    |Value|Use case|
    |-----|--------|
    |**Maximize**|Select if an increase in this indicator score is desired. For example, consider selecting **Maximize** for an indicator that shows revenue. Analytic tools and graphic elements reflect that an increase in this indicator score is good and a decrease is bad.|
    |**Minimize**|Select if a decrease in this indicator score is desired. For example, consider selecting **Minimize** for an indicator that shows costs. Analytic tools and graphic elements reflect that a decrease in this indicator score is good and an increase is bad.|
    |**None**|Select if the direction of change in this score does not matter to your business.|

6.  Define the Formula for this indicator.

    1.  To use a calculated value in the formula, click **Browse for a method** \(Repeatable\).

        A dialog opens for you to insert a method from PAFormulaUtils\(\) into the formula. This API returns the calculated value for an indicator. For more information about using this API, see [Get analytics methods in formulas](get-indicator-analytics.md).

        ![List of descriptive labels of methods in the "Add a method to the formula" dialog box, with Get global target gap of the specified indicator" highlighted.](../image/formula-method-selector.png)

    2.  To put the score of an indicator in the formula, click the **Browse for an indicator** link and fill in the dialog \(Repeatable\).

<table id="table_lqr_xwr_52b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indicator

</td><td>

The indicator you are inserting as a contributing indicator into the formula.If you use a business or fiscal calendar for this indicator, at least one indicator in the formula must use the matching calendar and calendar frequency.

</td></tr><tr><td>

Breakdown, Element, second-level Breakdown, second-level Element

</td><td>

Up to two levels of breakdown and element for filtering the scores on the indicator. If you specify a breakdown, you must specify an element of that breakdown. These breakdowns and elements apply only to this contributing indicator and not to the formula indicator as a whole.

</td></tr><tr><td>

Time series

</td><td>

A predefined analytical function, like a 7-days running average, to apply to the indicator instead of showing the raw scores of the indicator. This time series applies only to this contributing indicator and not to the formula indicator as a whole.

</td></tr><tr><td>

Allow breakdowns

</td><td>

Applies breakdowns that apply to the entire formula indicator, as opposed to individual indicators in the formula, to apply to this contributing indicator. Enabled by default. For more information, see [Prevent a contributing indicator in a formula from following breakdowns](../concept/c_ExcludingBreakdownsFromFormulas.md).Breakdowns are added to the entire formula through the **Manage breakdowns** dialog, available after the indicator is saved. See Step [11](t_CreateAFormulaIndicator.md#step_manage_breakdowns).

</td></tr><tr><td>

Use in method

</td><td>

Returns a unique identifier instead of the score for this indicator. Select this box when you are specifying an indicator for a method in the formula. These methods get calculated values for the indicator from the Analytics Hub. For more information about using these methods, see [Get analytics methods in formulas](get-indicator-analytics.md).

</td></tr></tbody>
</table>        You could add indicators manually. However, by using the **Browse for an indicator** function, you ensure that you have the proper notation for indicators and [breakdown elements](../concept/performance-analytics-glossary.md#).

        After you save the formula indicator, the indicators in the formula appear in the **Contributing indicators** related list. If you included any formula indicators, their contributing indicators are also listed.

    3.  Add mathematical operators and symbols to the **Formula** as needed.

        Enter any operators or numbers to include in the formula. Use valid operator symbols, such as +, -, /, %, &gt;, &lt;. You can also add more indicators to the formula. For example, to calculate the average age of open incidents based on summed age of open incidents and number of open incidents, use the following formula: `[[Summed age of open incidents]] / [[Open incidents]] / 24`

        To specify a data collection period in the formula, you can use the variables `score_start` and `score_end` to refer to the start and end of the data collection period, respectively. However, see the caveats in [Changes to score\_start/end because of different user time zones](../concept/time-zones-indicator-formulas.md).

        **Warning:** Try not to use GlideRecords or GlideAggregates in Performance Analytics scripts or formula indicators. While sometimes you must use these operations to get what you want, they are expensive, potentially running hundreds of thousands of times. Be certain that no alternative exists before you use them.

7.  In the **Access control** tab, set whether to save this indicator to the library and whether to limit the visibility of the indicator by user, group, or role.

8.  In the **Other** tab, set miscellaneous properties.

    These properties apply to the entire formula indicator.

<table id="table_rk2_zls_52b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default time series

</td><td>

A predefined analytical function, such as a 7-day running average. Depending on whether **Apply time series to result** is set, this time series can apply either to each component indicator before the result is calculated, or to the result.

</td></tr><tr><td>

Live group profile

</td><td>

Live Group Profile \[live\_group\_profile\] record for a Live Feed group. Specify a group profile to cause that group to get notifications about this indicator.

 For more information about this social application on the ServiceNow AI Platform, see [Live Feed](https://www.servicenow.com/docs/access?context=c_GetStartedWithLiveFeed&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Order

</td><td>

Number indicating the order in which indicators are displayed in the Analytics Hub. Indicators with the lowest value are displayed at the top of the list. If no values are provided in the **Order** field, indicators are displayed from a to z using the **Name** field. To use the order field, you must enter order numbers for all indicators. If you put in numbers for only a few indicators, the order in which indicators are displayed reverts to a to z.

 Not used in Platform Analytics experience.

</td></tr><tr><td>

Render continuous lines

</td><td>

When selected, the Analytics Hub and KPI Details show unbroken data lines for this indicator, even when there is no data for a specific date. This behavior may be useful when displaying data sets with varied starting dates or for data that are not regularly updated, such as stock information.

 Continuous lines are not rendered when a time series is set on the indicator or the Analytics Hub or KPI Details.

</td></tr><tr><td>

Apply time series to result

</td><td>

Applies a time series aggregation to the result of the calculation of the formula instead of to each component indicator before the result is calculated. This option applies to a time series selected for the indicator on a widget or on the Analytics Hub. If a default time series is specified for the indicator, this option also applies to that time series. For more information, see [Applying time series to result or to contributing indicators](../concept/apply-time-series-result-components.md).

</td></tr><tr><td>

Allow formula component to be NULL

</td><td>

Has the formula calculated even when it contains a null score. Useful for troubleshooting. For more information, see [Detect indicators with no scores in a formula](detect-indicators-no-scores-formula.md).

</td></tr><tr><td>

Allow aggregation of multiple breakdown element scores

</td><td>

Enables widgets to show the summed score of multiple breakdown elements on this indicator. If this field is selected, you can select either aggregated or separated values on the form for a breakdown dashboard that uses this indicator. Formulas based on addition, subtraction, or multiplication are generally good candidates for allowing aggregation. Percentages are also supported, provided the percentages total to 100%. On the other hand, the results of aggregating elements on averages, or of percentages that are not related, are usually not meaningful. **Warning:** These aggregations are not checked for mathematical validity.

</td></tr></tbody>
</table>9.  In the **Forecasting** tab, set the forecast method, the number of data collection periods to forecast, the amount of historical data to base the forecast on, and the upper and lower limits of forecast values.

    For more information, see [Performance Analytics scores forecasts](../concept/c_ForecastingData.md#).

10. Expand the context menu and click **Save**.

    ![Save option in the context menu](../image/auto-indicator-save.png)

11. To apply a breakdown to the entire formula indicator, click **Manage breakdowns** at the top of the page.

    By default, you can apply only breakdowns that are configured for every contributing indicator in the formula.

    **Note:** The system property **com.snc.pa.formula\_indicator\_valid\_breakdown** controls this behavior. By default, it is true. Changing it to false allows you to apply a breakdown to a formula indicator when at least one contributing indicator uses that breakdown. Attempts to view scores for unsupported breakdowns in a widget, the Analytics Hub, or KPI Details result in a warning message instead of a value.

    You cannot select a breakdown element in the formula indicator record. The breakdown can only be used interactively, meaning on the Analytics Hub, KPI Details, appropriately configured data visualizations, and dashboards. For information about using the **Manage breakdowns** tool, see [Assign and map breakdowns](create-breakdown-mapping.md#).


## Incident Backlog Growth

As an Incident Manager, you want to improve the efficiency of incident resolution. You already track new and resolved incidents as the Number of new incidents and Number of resolved incidents indicators. However, these indicators do not tell you if you are achieving your goal of improving incident resolution.

You need a new Backlog Growth KPI to measure the volume of outstanding incidents. To implement this KPI, you create a formula indicator named Incident Backlog Growth, with the following formula:

```
[[Number of new incident]] - [[Number of resolved incidents]]
```

![Incident backlog growth indicator record.](../image/incident-backlog-growth.png)

By turning on **Show in library**, you make the indicator visible in KPI Details. In the information panel on KPI Details, you can see the formula used in the indicator.

![The Incident Backlog Growth indicator in KPI Details](../image/formula-indic-incident-bklog-growth.png)

**Parent Topic:**[Formula indicators](../concept/formula-indicators.md)

**Related topics**  


[Get analytics methods in formulas](get-indicator-analytics.md)

[Prevent a contributing indicator in a formula from following breakdowns](../concept/c_ExcludingBreakdownsFromFormulas.md)

[Breakdown matrices in formula indicators](../concept/bkdown-matrix-formula-indicators.md)

[Applying time series to result or to contributing indicators](../concept/apply-time-series-result-components.md)

[Detect indicators with no scores in a formula](detect-indicators-no-scores-formula.md)

[Indexing multiple indicators in a formula](../concept/index-indicators.md)

[Changes to score\_start/end because of different user time zones](../concept/time-zones-indicator-formulas.md)

