---
title: Activate Data snapshots
description: Enable Data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When Data snapshots are enabled, you can apply multiple breakdown levels to an indicator.You can edit an indicator record so the indicator is eligible for Data snapshots, then activate Data snapshots for that indicator from the record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/activate-unlimited-breakdowns.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Activate Data snapshots

Enable Data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When Data snapshots are enabled, you can apply multiple breakdown levels to an indicator.

## Before you begin

You have to meet the following requirements:

-   Your instance must be running the RaptorDB Professional database.
-   The Data Snapshots \(com.snc.pa.mlb\) plugin must be activated on the instance.Starting with Australia Patch 3, if the instance is eligible, this plugin is installed automatically.
-   To use Data snapshots on a production instance, you must have a subscription to Performance Analytics as described in [Activating your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PremiumPerformanceAnalytics.md). On a non-production instance, activate any of the Performance Analytics Premium plugins.
-   Your instance must not be domain-separated.

**Warning:** Data snapshots is deactivated on the instance if the Data Snapshots plugin is deactivated or domain separation is activated. If you want to re-activate Data snapshots on such an instance, contact Now Support.

Role required: pa\_data\_collector or higher

## About this task

Certain indicators support more than two levels of breakdown. This feature is called multiple breakdowns, and is one of the features of Data snapshots. This feature is not available for all indicators. For a list of restrictions, see [Limitations and requirements for Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/limitations-mlb.md).Activate Data snapshots for each eligible indicator, either one-at-a-time or in bulk.

**Important:** Classic Performance Analytics data collection jobs continue to run in parallel on indicators that have Data snapshots enabled. The scores that the classic job collects are not used while Data snapshots are enabled. Parallel job collection ensures smooth rollback if necessary.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Indicators**.

2.  Press **Check instance eligibility** to see if your instance is eligible for Data snapshots and, if not, why.

    When your instance is eligible for Data snapshots, you have a banner announcing this fact and two new tiles, Data snapshots enabled and Data snapshots supported.

    \[Omitted image "kpis-ds-enabled.png"\] Alt text: Indicator library with Data snapshots eligible on the instance.

3.  Expand **Edit list columns** \[Omitted image "edit-list-columns.png"\] Alt text: Edit list columns button and tooltip. and add the Data snapshots status and Fact table row count columns.

    If the number of table rows exceeds the license limit, the column Fact table row count has the value `true`.

    \[Omitted image "edit-columns.png"\] Alt text: Adding the Data snapshots status column to the Indicator library.

4.  To filter the list, you can select the **Data snapshots supported** tile.

5.  Select one or more indicators in the list and press **Enable Data Snapshots \(quantity of indicators selected\)**.

    If an indicator source table size exceeds either the number of rows restricted by your license or technical storage limitations, you receive a warning.

    \[Omitted image "ds-table-size-modal.png"\] Alt text: Modal that your facts table has exceeded size limitations for activating Data snapshots.


## Result

All eligible selected indicators now have Data snapshots enabled and thus support multiple levels of breakdown.

## What to do next

To see why a specific indicator does not support Data snapshots \(Data snapshots status = unsupported\), you can examine its indicator record. Select the Edit icon \[Omitted image "edit-icon.png"\] Alt text: Edit icon for that indicator to open its record. Decide whether to alter the indicator and try to activate Data snapshots for it.

**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

**Related topics**  


[Create an automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreateAnAutomatedIndicator.md)

[Create a formula indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreateAFormulaIndicator.md)

[Create a Data snapshots automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-ds-automated-indicator.md)

[Create a Data snapshots formula indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-ds-formula-ind.md)

## Activate Data snapshots for a single indicator

You can edit an indicator record so the indicator is eligible for Data snapshots, then activate Data snapshots for that indicator from the record.

### Before you begin

Role required:

-   If an appropriate Data snapshots source already exists: pa\_data\_collector, pa\_power\_user, or higher.
-   If an appropriate Data snapshots source must be generated: pa\_data\_collector or higher. Users with pa\_power\_user receive an error message.

### Procedure

1.  Locate the indicator in the indicator library.

2.  Select Edit \[Omitted image "edit-icon.png"\] Alt text: Edit icon to open the indicator record.

    If you had previously tried unsuccessfully to enable Data snapshots for this indicator, you see a message explaining the reasons the indicator did not qualify.

    \[Omitted image "ds-indicator-unsupported-reasons.png"\] Alt text: Example message of reasons an indicator does not support Data snapshots.

3.  Address the reasons that the indicator did not qualify for Data snapshots.

4.  Save the indicator.

5.  Select **Enable Data Snapshots**.

    \[Omitted image "indicator-top-right-buttons.png"\] Alt text: The enable Data snapshots button on an indicator record.

    A modal opens explaining the process of enabling Data snapshots:

    -   That the indicator will be linked to an appropriate [Data snapshots source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/tables-unlimited-breakdowns.md) if one exists
    -   That if no suitable Data snapshots source exists, one will be created
    -   Which of the requirements for Data snapshots are met or not met
    -   Whether the record volume is within the allowed threshold for your license
6.  If you meet all the requirements and agree with the process, select **Continue**.


### Result

When you activate multiple breakdowns, you override any calendar and frequency you have set on the indicator. The indicator becomes daily.

When Data snapshots are enabled, the indicator has two data sources: the original indicator source and a Data snapshots source. You continue to see the original, classic indicator source in the **Indicator source** field, with a link to the Data snapshots source.

\[Omitted image "classic-and-ds-sources.png"\] Alt text: Classic and Data snapshots sources in Source tab of indicator record.

Classic Performance Analytics data collection jobs continue to run in parallel on indicators that have Data snapshots enabled. The scores that the classic job collects are not used while Data snapshots are enabled. If Data snapshots are disabled for the indicator, scores collected from the classic source are used, so you have no gap in your indicator scores.

