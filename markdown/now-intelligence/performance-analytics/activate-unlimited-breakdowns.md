---
title: Activate data snapshots
description: Enable data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When data snapshots are enabled, you can apply multiple breakdown levels to an indicator.You can edit an indicator record so the indicator is eligible for data snapshots, then activate data snapshots for that indicator from the record.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Activate data snapshots

Enable data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When data snapshots are enabled, you can apply multiple breakdown levels to an indicator.

## Before you begin

You have to meet the following requirements:

-   Your instance must be running the RaptorDB Professional database.
-   The Data Snapshots \(com.snc.pa.mlb\) plugin must be activated on the instance.
-   To use data snapshots on a production instance, you must have a subscription to Performance Analytics as described in [Activating your Performance Analytics subscription](../concept/c_PremiumPerformanceAnalytics.md#). On a non-production instance, activate any of the Performance Analytics Premium plugins.
-   Your instance must not be domain-separated.

**Warning:** Data snapshots is deactivated on the instance if the Data Snapshots plugin is deactivated or domain separation is activated. If you want to re-activate data snapshots on such an instance, contact Now Support.

Role required: pa\_data\_collector or higher

## About this task

Certain indicators support more than two levels of breakdown. This feature is called multiple breakdowns, and is one of the features of data snapshots. This feature is not available for all indicators. For a list of restrictions, see [Limitations and requirements for data snapshots](../reference/limitations-mlb.md).

You have to activate data snapshots for the instance by enabling the Data Snapshots \(com.snc.pa.mlb\) plugin. You then have to activate data snapshots for each indicator, either one-at-a-time or in bulk.

**Important:** Classic Performance Analytics data collection jobs continue to run in parallel on indicators that have data snapshots enabled. The scores that the classic job collects are not used while data snapshots are enabled. Parallel job collection ensures smooth rollback if necessary.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Indicators**.

2.  Press **Check instance eligibility** to see if your instance is eligible for data snapshots and, if not, why.

    When your instance is eligible for data snapshots, you have a banner announcing this fact and two new tiles, Data snapshots enabled and Data snapshots supported.

    ![Indicator library with data snapshots eligible on the instance.](../../par-for-workspace/image/kpis-ds-enabled.png)

3.  Expand **Edit list columns** ![Edit list columns button and tooltip.](../image/edit-list-columns.png) and add the Data snapshot status and Fact table row count columns.

    If the number of table rows exceeds the license limit, the column Fact table row count has the value `true`.

    ![Adding the Data snapshot status column to the Indicator library.](../image/edit-columns.png)

4.  To filter the list, you can select the **Data snapshots supported** tile.

5.  Select one or more indicators in the list and press **Enable Data Snapshots \(quantity of indicators selected\)**.

    If an indicator source table size exceeds either the number of rows restricted by your license or technical storage limitations, you receive a warning.

    ![Modal that your facts table has exceeded size limitations for activating data snapshots.](../image/ds-table-size-modal.png)

6.  If you are warned about indicator source table size, you can choose to exclude the affected indicators and continue with enabling data snapshots.


## Result

All eligible selected indicators now have data snapshots enabled and thus support multiple levels of breakdown.

## What to do next

To see why a specific indicator does not support data snapshots \(Data snapshots status = unsupported\), you can examine its indicator record. Select the Edit icon ![Edit icon](../../../administer/process-mining/image/edit-icon.png) for that indicator to open its record. Decide whether to alter the indicator and try to activate data snapshots for it.

**Parent Topic:**[Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md)

**Related topics**  


[Create an automated indicator](t_CreateAnAutomatedIndicator.md#)

[Create a formula indicator](t_CreateAFormulaIndicator.md)

## Activate data snapshots for a single indicator

You can edit an indicator record so the indicator is eligible for data snapshots, then activate data snapshots for that indicator from the record.

### Before you begin

Role required: pa\_data\_collector, pa\_power\_user, or higher

### Procedure

1.  Locate the indicator in the indicator library.

2.  Select Edit ![Edit icon](../../../administer/process-mining/image/edit-icon.png) to open the indicator record.

    If you had previously tried unsuccessfully to enable data snapshots for this indicator, you see a message explaining the reasons the indicator did not qualify.

    ![Example message of reasons an indicator does not support data snapshots.](../image/ds-indicator-unsupported-reasons.png)

3.  Address the reasons that the indicator did not qualify for data snapshots.

4.  Save the indicator.

5.  Select **Enable Data Snapshots**.

    ![The enable data snapshots button on an indicator record.](../image/indicator-top-right-buttons.png)

    A modal opens explaining the process of enabling data snapshots:

    -   That the indicator will be linked to an appropriate [data snapshots source](../reference/tables-unlimited-breakdowns.md) if one exists
    -   That if no suitable data snapshots source exists, one will be created
    -   Which of the requirements for data snapshots are met or not met
    -   Whether the record volume is within the allowed threshold for your license
6.  If you meet all the requirements and agree with the process, select **Continue**.


### Result

When you activate multiple breakdowns, you override any calendar and frequency you have set on the indicator. The indicator becomes daily.

When data snapshots are enabled, the indicator has two data sources: the original indicator source and a data snapshots source. You continue to see the original, classic indicator source in the **Indicator source** field, with a link to the Data snapshots source.

![Classic and data snapshots sources in Source tab of indicator record.](../image/classic-and-ds-sources.png)

Classic Performance Analytics data collection jobs continue to run in parallel on indicators that have data snapshots enabled. The scores that the classic job collects are not used while data snapshots are enabled. If data snapshots are disabled for the indicator, scores collected from the classic source are used, so you have no gap in your indicator scores.

