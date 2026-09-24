---
title: Sources and records for enabled Data snapshots indicators
description: When you enable Data snapshots for an existing automated indicator, that indicator is associated with a Data snapshots source. The indicator follows the source's time zone. You might need to change the calendar frequency.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/ds-score-collection-enabled-indicators.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [data snapshots, automated indicator, enabled, calendar frequency]
breadcrumb: [Activate Data snapshots, Data snapshots and multiple breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Sources and records for enabled Data snapshots indicators

When you enable Data snapshots for an existing automated indicator, that indicator is associated with a Data snapshots source. The indicator follows the source's time zone. You might need to change the calendar frequency.

When you enable Data snapshots for an indicator, a Data snapshots indicator record is created for it. The original record still exists.

If you enable an automated indicator, a Data snapshots source is linked to the new Data snapshots automated indicator record. The system first searches for an appropriate existing Data snapshots source. If the system does not find such a source, a Daily source is created. If the time zone of the indicator and of the Data snapshots source do not match, the time zone of the source takes precedence. The original, classic indicator record is still associated with the classic indicator source.

If you enable a formula indicator, the new record is linked to Data snapshots contributing indicators. The original, classic indicator record is still linked to the classic contributing indicators.

Classic data collection jobs still run on enabled Data snapshots indicators, running alongside Data snapshots. However, their scores are not shown. Instead, the new Data snapshots scores are shown. If Data snapshots are later disabled for the indicator, the Data snapshots scores are replaced with the contemporaneous classic scores.

**Warning:** You can disable the classic collection jobs manually for Data snapshots indicators. However, if you disable those jobs and later disable Data snapshots, those indicators will have no scores for the period when Data snapshots was enabled.

For an automated indicator, different calendars may be available than were in the classic source. If the Data snapshots-enabled automated indicator is linked to an **All changes** data source, the indicator supports whatever calendar frequencies that source supports. These frequencies may include intraday work shifts, for example. To check the calendar and calendar frequency, navigate to **All** &gt; **Data Snapshots** &gt; **Indicators** &gt; **Automated Indicators - Data Snapshots**. Locate and open your indicator. Then select the calendar and calendar frequency as described in [Create a Data snapshots automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/create-ds-automated-indicator.md).

**Note:** You can end up with a change in the pattern of indicator scores when you enable Data snapshots, for example if you change from daily collection to work shifts. Even if you keep the same calendar frequency, the switch to having scores shown in the user's time zone instead of the classic collection job's time zone can produce a change.

**Parent Topic:**[Activate Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/activate-unlimited-breakdowns.md)

