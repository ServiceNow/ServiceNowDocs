---
title: Add contributing indicators
description: Add new contributing indicators based on your organizational preferences.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-success-dashboard-indicators/add-contributing-indicators.html
release: australia
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [KPI configuration for Success Dashboard indicators, ITSM Success Dashboard Admin console, Configure, ITSM Success Dashboard indicators, IT Service Management]
---

# Add contributing indicators

Add new contributing indicators based on your organizational preferences.

## Before you begin

Role required: sn\_sd.success\_dashboard\_admin

## About this task

Your organization can add the new contributing sources as the primary indicator. For example, determining the automated catalog request completions can be added to Automated Resolutions.

## Procedure

1.  Create a Performance Analytics \(PA\) indicator and its data collection job that measures the daily score \(count\) of the metric that you need to measure.

    The description set for this PA indicator is used to describe the indicator when the user selects the information icon on the score card. Alternatively, if you already have a PA indicator that measures daily scores of the metric you need to measure, you can directly proceed to register and use the PA indicator.

    For information about permissions required to create a PA indicator, see [Performance Analytics roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/r_PARoles.md).

2.  Register the PA indicator against the Primary Indicator that it must be reported in by creating a record in the Contributing Indicator Registry \[sn\_sd\_contributing\_indicator\_registry\] table.

    1.  Navigate to **All** &gt; **sn\_sd\_contributing\_indicator\_registry.list**.

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
</table>    4.  Open the context menu for the header and select **Save**.

    5.  Add More information context cards for this indicator so that the user viewing the primary and contributing indicator details understands this KPI.

        See [Update more information cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/update-sidepanel-more.md) for details.

    6.  In the Persona Group Time Savings related list, select **New**.

    7.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Persona Group|Option to select the persona group for the contributing indicator.|
        |Time saved|Option to enter the time that is saved to complete the request.|

    8.  Open the context menu for the header and select **Save**.

        **Note:** You can also update the values for the indicators in **Persona Group Time Savings** section for the base system indicators that are **Automatic** type.


**Parent Topic:**[KPI configuration for Success Dashboard indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/config-kpis-sdb.md)

