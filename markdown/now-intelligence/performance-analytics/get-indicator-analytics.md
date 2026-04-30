---
title: Get analytics methods in formulas
description: To insert a calculated value from the Analytics Hub into a formula, use a method in the formula.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Formula indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Get analytics methods in formulas

To insert a calculated value from the Analytics Hub into a formula, use a method in the formula.

## Before you begin

Role required: pa\_power\_user, admin

## About this task

You can use a value that was calculated in the Analytics Hub as input for a formula. That value can be from any indicator, including from the current formula indicator itself.

To get a value from the Analytics Hub, insert a method from PAFormulaUtils\(\) into the formula. To call one of these methods, use the Performance Analytics variable `pa`. For example, to use the PAFormulaUtils.getScore method, call `pa.getScore`. For more information, see [PAFormulaUtils API](../PAFormulaUtil/concept/PAFormulaUtils.md).

## Procedure

1.  Open the formula indicator record.

2.  Beneath the Formula box, click **Browse for a method**.

    A dialog box opens where you can select a method.

3.  Browse for the method that matches your needs.

    Methods refer either to the current formula that you are editing or to a different indicator that you must specify. The list shows a descriptive label for each method instead of the method name.

    ![List of descriptive labels of methods in the "Add a method to the formula" dialog box, with Get global target gap of the specified indicator" highlighted.](../image/formula-method-selector.png)

4.  Select a method.

    When you select a method, a description opens, including the name of the method and any parameter fields.

    ![The Add a method to the formula dialog showing the method Get global target gap of the specified indicator selected and the date specified as the last score collected](../image/formula-indic-method-desc.png)

    Date fields can take the following values:

    -   An absolute date in YYYY-MM-DD format, such as 2018-12-21.
    -   The variable `score_start` or `score_end`. These variables represent the first and last second of the collection period being calculated for the referenced indicator. The times are calculated from the difference between the time zone of the user and the database server time zone, which is GMT. For more information, see [Changes to score\_start/end because of different user time zones](../concept/time-zones-indicator-formulas.md).
    -   A date parameter that you have coded yourself using the GlideDate or the GlideDateTime API.
5.  Fill in any parameters and click **Select**.

    The dialog closes and the method appears in the formula field of the indicator form.

6.  If the method requires you to specify an indicator, select the `indicator` parameter with the cursor and click **Browse for an indicator**.

    The indicator selection dialog opens.

    ![Opening the indicator selection dialog from inside a method in the formula](../image/formula-method-browse-indicator.gif)

7.  Select the indicator.

8.  Select any breakdowns or elements and a time series aggregation.

9.  Select **Use in method** and click **Submit**.

    The method is complete, with an indicator selected. Note that a dollar sign, $, precedes the indicator. This dollar sign means that the Analytics Hub values for the indicator instead of the indicator score are returned. The Analytics Hub values are selected instead of the score when you select the **Use in method** check box.

    ![Indicator, breakdown, element, and Use in method check box being selected](../image/formula-method-select-indicator.gif)


## Index indicator

Index indicators are a use case of formula indicators for generating a single score that represents multiple indicators. In the following example, you want a single index that aggregates the gap between score and global target for the following indicators:

-   The percentage of incidents that are overdue.
-   The average age of the last update of open incidents.
-   The total number of open incidents.

To get this single index, you create a formula indicator with **Direction** set to **Maximize**. All index indicators must maximize. Then you use the **Browse for a method** and **Browse for an indicator** functions to create the following formula:

```
var a = pa.getGap($[[% of open overdue incidents]], score_start) / pa.getGlobalTarget($[[% of open overdue incidents]],score_start);
var b = pa.getGap($[[Average age of last update of open incidents]], score_start) / pa.getGlobalTarget($[[Average age of last update of open incidents]], score_start);
var c = pa.getGap($[[Number of open incidents]], score_start) / pa.getGlobalTarget($[[Number of open incidents]], score_start);
var res = 100 - (100 * (a + b + c) / 3);
res;
```

## Set targets on a change itself

You want to set a target for your teams of a 10% reduction month-on-month in the incident backlog. You create a formula indicator with the following formula, and set a target of -10% for this indicator on the Analytics Hub.

```
var lastPeriod = new GlideDateTime(score_start.getYearUTC() + '-' + score_start.getMonthUTC() + '-01');
lastPeriod.addDaysUTC(-1);
pa.getChangePercentage($[[Number of open incidents]], lastPeriod.addDaysUTC(-1), score_start);
```

## Filter out scores based on breakdown and element

You want to filter out the scores of incidents where Priority = 1 - Critical.

1.  Obtain the unique record identifiers for the Priority breakdown and the 1 - Critical element. Breakdown records are in the Breakdown table. The location of element records varies, but is identified in the Breakdown Source of the breakdown. In this case, the element is a Choice \[sys\_choice\] record. For directions on how to obtain the unique record identifiers, see [The unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    The unique record identifiers are baec0752bf130100b96dac808c0739ed for the Priority breakdown and 8a4dde73c6112278017a6a4baf547aa7 for the 1 - Critical element.

2.  Create an indicator with the following formula:

    ```
    var res = [[Number of open incidents]];
    if(pa.getCurrentBreakdownID() == 'baec0752bf130100b96dac808c0739ed' && pa.getCurrentElementID() == '8a4dde73c6112278017a6a4baf547aa7')
    {
    res = 0;
    }
    res;
    ```


-   **[PAFormulaUtils API](../PAFormulaUtil/concept/PAFormulaUtils.md)**  
The PAFormulaUtils API enables you to obtain a value that was calculated in the Analytics Hub and use that value as input for a formula.

**Parent Topic:**[Formula indicators](../concept/formula-indicators.md)

**Related topics**  


[Create a formula indicator](t_CreateAFormulaIndicator.md)

[Prevent a contributing indicator in a formula from following breakdowns](../concept/c_ExcludingBreakdownsFromFormulas.md)

[Breakdown matrices in formula indicators](../concept/bkdown-matrix-formula-indicators.md)

[Applying time series to result or to contributing indicators](../concept/apply-time-series-result-components.md)

[Detect indicators with no scores in a formula](detect-indicators-no-scores-formula.md)

[Indexing multiple indicators in a formula](../concept/index-indicators.md)

[Changes to score\_start/end because of different user time zones](../concept/time-zones-indicator-formulas.md)

