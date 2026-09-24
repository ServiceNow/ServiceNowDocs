---
title: Activate Data snapshots for a single indicator
description: You can edit an indicator record so the indicator is eligible for Data snapshots, then activate Data snapshots for that indicator from the record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/activate-ds-single-indicator.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Activate Data snapshots, Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Activate Data snapshots for a single indicator

You can edit an indicator record so the indicator is eligible for Data snapshots, then activate Data snapshots for that indicator from the record.

## Before you begin

Role required:

-   If an appropriate Data snapshots source already exists: pa\_data\_collector, pa\_power\_user, or higher.
-   If an appropriate Data snapshots source must be generated: pa\_data\_collector or higher. Users with pa\_power\_user receive an error message.

## Procedure

1.  Locate the indicator in the indicator library.

2.  Select Edit \[Omitted image "edit-icon.png"\] Alt text: Edit icon to open the indicator record.

    If you had previously tried unsuccessfully to enable Data snapshots for this indicator, you see a message explaining the reasons the indicator did not qualify.

    \[Omitted image "ds-indicator-unsupported-reasons.png"\] Alt text: Example message of reasons an indicator does not support Data snapshots.

3.  Address the reasons that the indicator did not qualify for Data snapshots.

4.  Save the indicator.

5.  Select **Enable Data Snapshots**.

    \[Omitted image "indicator-top-right-buttons.png"\] Alt text: The enable Data snapshots button on an indicator record.

    A modal opens explaining the process of enabling Data snapshots:

    -   That the indicator will be linked to an appropriate [Data snapshots source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/tables-unlimited-breakdowns.md) if one exists
    -   That if no suitable Data snapshots source exists, one will be created
    -   Which of the requirements for Data snapshots are met or not met
    -   Whether the record volume is within the allowed threshold for your license
6.  If you meet all the requirements and agree with the process, select **Continue**.


## Result

When you activate Data snapshots for an indicator, the indicator is linked to an All Activity data source if one exists. Intraday score collection is thereby supported.

When Data snapshots are enabled, the indicator has two data sources: the original indicator source and a Data snapshots source. You continue to see the original, classic indicator source in the **Indicator source** field, with a link to the Data snapshots source.

\[Omitted image "classic-and-ds-sources.png"\] Alt text: Classic and Data snapshots sources in Source tab of indicator record.

Classic Performance Analytics data collection jobs continue to run in parallel on indicators that have Data snapshots enabled. The scores that the classic job collects are not used while Data snapshots are enabled. If Data snapshots are disabled for the indicator, scores collected from the classic source are used, so you have no gap in your indicator scores.

**Important:** Classic Performance Analytics data collection is not run on native Data snapshots indicators.

**Parent Topic:**[Activate Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/activate-unlimited-breakdowns.md)

