---
title: Performance Analytics release notes
description: The ServiceNow   Performance Analytics application is an in-platform process optimization solution. It enables  organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced  and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Performance Analytics release notes

The ServiceNow®   Performance Analytics application is an in-platform process optimization solution. It enables  organizations to set, track, and analyze progress toward goals. Performance Analytics was enhanced  and updated in the Australia release.

## Performance Analytics highlights for the Australia release

**Note:** The highlights for this release all refer to the newer Data Snapshots indicator architecture, which requires RaptorDB Professional.

-   Create new Data snapshots indicators with unlimited breakdowns. Previously you could convert only existing indicators. These indicators are supported in Data Visualizations and in KPI Details.
-   Track intraday changes with indicators such as changes between shifts. You can track changes in shifts that are still in progress, with data retrieved down to the minute level.
-   View scores as they accumulate throughout the day without having to wait for end-of-day processing.
-   When exploring a Data snapshots indicator with KPI Details, customizable score formats, apply flexible breakdowns and aggregation periods, direct alert subscriptions for targets and thresholds, and apply hierarchical roll-ups for breakdowns.

See Performance Analytics \(Indicator data sources\) for more information.

## New in the Australia release

-   **Create data snapshots indicators**

    Create data snapshots indicators and their sources rather than being able to enable data snapshots only on existing indicators. Benefit from the simplicity of data snapshots indicators, including the escape from the two-level breakdown limit. You can create either automated or formula indicators. Access control for these indicator is the same as for classic Performance Analytics indicators.

-   **Create intraday indicators**

    Track process changes at a more granular level than daily, such as by work shift. Data snapshots indicator sources support business calendars with intraday periods, which can be as short as per minute.


## Changed in this release

-   **Explore native data snapshots indicators with KPI Details**

    KPI Details supports data snapshots indicators that you create, not only those that are enabled from classic indicators. The following features have been created for or extended to native data snapshots indicators:

    -   Subscriptions for alerts on targets and thresholds, which can be set from the targets and thresholds panels
    -   Adjustable filtering by breakdown, calendar, or time series aggregation
    -   Hierarchical breakdowns, with scores rolled up to parent elements
    -   Customizable score formatting options, such as precision and abbreviation
-   **View data trends in data snapshots as data accumulates**

    When you select a field by which to trend a data snapshots automated indicator, you have the option to show the trend for incomplete collection periods. This feature shows the trend as it develops for live data without having to wait for the end of the collection period. You can set this behavior either on the automated data snapshot indicator record or in a time series data visualization for a data snapshot indicator.

-   **Collect data snapshots scores with confidence**

    Data mining for data snapshots scores has the following improvements:

    -   Collect scores for tables with any volume of records.
    -   The system accurately and automatically handles data gaps when data mining is disabled.
    -   You are warned of the implications before you manually disable data mining \(score collection\).
-   **Activate data snapshots in more cases and with better information**
    -   Activate indicators without active data collector jobs.
    -   Activate indicators regardless of underlying record volume. For example, the `INSERT_VOLUME_EXCEEDED` error no longer occurs.
    -   If the activation fails because of scripted breakdowns, the scripted breakdowns are listed in the failure message.
    -   Generic parsing errors have been rewritten into specific, categorized messages.

## Deprecated features

-   The **Dashboard Visualization** tab in KPI Composer is no longer supported. Existing data visualization tabs remain but you are not able to create new ones because this feature is connected to Core UI dashboards, which are themselves deprecated.
-   Performance Analytics widgets are deprecated along with Core UI dashboards. Users with the pa\_admin role are still able to create Performance Analytics widgets.
-   The Analytics Hub has been replaced by KPI Details. Attempts to open the Analytics Hub are redirected to KPI Details.

## Activation information

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this complimentary application.

The full features of Performance Analytics are available with a subscription. Activate the Premium plugin that matches your subscription. For details, see Activating your Performance Analytics subscription.

## Related ServiceNow applications and features

-   **Platform Analytics experience**

    The ServiceNow® Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products, including Performance Analytics.

-   **Process Mining**

    Process Mining helps analysts and process owners quickly analyze and optimize their business processes. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.


**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

