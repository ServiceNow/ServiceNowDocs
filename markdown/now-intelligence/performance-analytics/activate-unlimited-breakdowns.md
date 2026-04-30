---
title: Activate data snapshots
description: Enable data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When data snapshots are enabled, you can apply multiple breakdown levels to an indicator.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Data snapshots and multiple breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Activate data snapshots

Enable data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When data snapshots are enabled, you can apply multiple breakdown levels to an indicator.

## Before you begin

The Data Snapshots \(com.snc.pa.mlb\) plugin must be activated on the instance. You also must have a subscription to Performance Analytics to use data snapshots on a production instance, as described in [Activating your Performance Analytics subscription](../concept/c_PremiumPerformanceAnalytics.md#). On a non-production instance, activate any of the Performance Analytics Premium plugins.

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

3.  To set an individual indicator to support more than two levels of breakdown, perform the following actions:

    1.  Open the indicator record.

    2.  Select **Enable Data Snapshots**.

        ![The enable data snapshots button on an indicator record.](../image/indicator-top-right-buttons.png)

        A modal opens explaining the process of enabling data snapshots:

        -   That the indicator will be linked to an appropriate [data snapshots source](../reference/tables-unlimited-breakdowns.md) if one exists
        -   That if no suitable data snapshots source exists, one will be created
        -   Which of the requirements for data snapshots are met or not met
        -   Whether the record volume is within the allowed threshold for your license
    3.  If you meet all the requirements and agree with the process, select **Continue**.


## What to do next

The scheduled conversion process runs hourly and synchronizes any changes to existing indicators. The job also converts any newly created indicators. To trigger the conversion process and sync changes manually, select **Update Data Snapshots status**. For example, manually synchronize changes after you have fixed an unsupported indicator configuration and you now want to enable data snapshots for that indicator.

If data snapshots were not enabled on some of the indicators, the indicator record contains a message giving the reasons why that indicator was not compatible. You also get suggestions about how to make the indicator compatible.

**Parent Topic:**[Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md)

**Related topics**  


[Create an automated indicator](t_CreateAnAutomatedIndicator.md#)

[Create a formula indicator](t_CreateAFormulaIndicator.md)

