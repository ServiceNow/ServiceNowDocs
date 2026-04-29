---
title: Add contributing indicators
description: Add new contributing indicators based on your organizational preferences.
locale: en-US
release: australia
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Success Dashboard indicators KPIs, ITSM Success Dashboard Admin console, Configure, ITSM Success Dashboard indicators, IT Service Management]
---

# Add contributing indicators

Add new contributing indicators based on your organizational preferences.

## Before you begin

Role required: sn\_sd.success\_dashboard\_admin

## About this task

Your organization can add the new contributing sources as the primary indicator. For example, determining the automated catalog request completions can be added to Automated Resolutions.

## Procedure

1.  Create a Performance Analytics \(PA\) indicator and its data collection job that measures the daily score \(count\) of the metric that you want to measure.

    The description set for this PA indicator is used to describe the indicator when the user selects the information icon on the score card. Alternatively, if you already have a PA indicator that measures daily scores of the metric you want to measure, you can directly proceed to register and use the PA indicator.

    For information on permissions required to create a PA indicator, see [Performance Analytics roles](https://www.servicenow.com/docs/access?context=r_PARoles&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) for more details.

2.  Register the PA indicator against the Primary Indicator that it must be reported in by creating a record in the Contributing Indicator Registry table \(sn\_sd\_contributing\_indicator\_registry\).

    1.  Navigate to **All &gt; sn\_sd\_contributing\_indicator\_registry.list**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_mht_s4h_cqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique identifier contributing indicator.

</td></tr><tr><td>

Contributing Indicator

</td><td>

Performance Analytics indicator of the metric.

</td></tr><tr><td>

Primary KPI

</td><td>

The primary indicator where the new indicator is being added to.

</td></tr><tr><td>

Service group

</td><td>

Service group of the performance indicator.**Note:** ITSM or HR must be selected as a service group, as required.

</td></tr></tbody>
</table>    4.  Right-click the header and select **Save**.

    5.  Add More information context cards for this indicator so that the user viewing the primary and contributing indicator details understands this KPI.

        See [Update more information cards](update-sidepanel-more.md) for details.

    6.  In the **Persona Group Time Savings** related list, click **New**.

    7.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Persona Group|Option to select the persona group fr the contributing indicator.|
        |Time saved|Option to enter the time that will be saved to complete the request.|

    8.  Right-click the header and select **Save**.

        **Note:** You can also update the values for the indicators in **Persona Group Time Savings** section for the out of the box indicators that are **Automatic** type.


**Parent Topic:**[Configure Success Dashboard indicators KPIs](config-kpis-sdb.md)

