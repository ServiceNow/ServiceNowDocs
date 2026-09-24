---
title: Activate Data snapshots
description: Enable Data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When Data snapshots are enabled, you can apply multiple breakdown levels to an indicator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/activate-unlimited-breakdowns.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Activate Data snapshots

Enable Data snapshots on an instance as a whole and on individual existing indicators \(KPIs\) on the instance. When Data snapshots are enabled, you can apply multiple breakdown levels to an indicator.

## Before you begin

You have to meet the following requirements:

-   Your instance must be running the RaptorDB Professional database.
-   The Data Snapshots \(com.snc.pa.mlb\) plugin must be activated on the instance. If the instance is eligible, this plugin is installed automatically.
-   To use Data snapshots on a production instance, you must have a subscription to Performance Analytics as described in [Activating your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_PremiumPerformanceAnalytics.md). On a non-production instance, activate any of the Performance Analytics Premium plugins.
-   Your instance must not be domain-separated.

**Warning:** Data snapshots is deactivated on the instance if the Data Snapshots plugin is deactivated or domain separation is activated. If you want to re-activate Data snapshots on such an instance, contact Now Support.

Role required: pa\_data\_collector or higher

## About this task

Certain indicators support more than two levels of breakdown. This feature is called multiple breakdowns, and is one of the features of Data snapshots. This feature is not available for all indicators. For a list of restrictions, see [Limitations and requirements for Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/limitations-mlb.md). Activate Data snapshots for each eligible indicator, either one-at-a-time or in bulk.

**Important:** Classic Performance Analytics data collection jobs continue to run in parallel on indicators that have Data snapshots enabled. The scores that the classic job collects are not used while Data snapshots are enabled. Parallel job collection provides smooth rollback if necessary.

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

On automated indicators that have successfully had Data snapshots enabled, check the Data snapshots source. \(The source might not be available until the first Data snapshots job runs.\) If the source is for **All activity** and not only **Daily**, adjust the calendar and calendar frequency. For more information, see [Sources and records for enabled Data snapshots indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/ds-score-collection-enabled-indicators.md).

-   **[Activate Data snapshots for a single indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/activate-ds-single-indicator.md)**  
You can edit an indicator record so the indicator is eligible for Data snapshots, then activate Data snapshots for that indicator from the record.
-   **[Sources and records for enabled Data snapshots indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/ds-score-collection-enabled-indicators.md)**  
When you enable Data snapshots for an existing automated indicator, that indicator is associated with a Data snapshots source. The indicator follows the source's time zone. You might need to change the calendar frequency.

**Parent Topic:**[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md)

**Related topics**  


[Create an automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_CreateAnAutomatedIndicator.md)

[Create a formula indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_CreateAFormulaIndicator.md)

[Create a Data snapshots automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-ds-automated-indicator.md)

[Create a Data snapshots formula indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-ds-formula-ind.md)

