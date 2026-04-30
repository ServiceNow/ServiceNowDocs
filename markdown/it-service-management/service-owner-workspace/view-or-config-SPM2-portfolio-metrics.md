---
title: Configure Service Owner Workspace portfolio metrics
description: Decide which metrics to configure for your service portfolio to measure the performance of your service offerings in Service Owner Workspace.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Configure Service Owner Workspace portfolio metrics

Decide which metrics to configure for your service portfolio to measure the performance of your service offerings in Service Owner Workspace.

## Before you begin

Role required: admin or portfolio\_admin

## About this task

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. Customers who opt in for the new standard portfolio structure use metrics calculated from key performance indicators \(KPIs\) in Digital Portfolio Management \(DPM\). For more information, see [Digital Portfolio Management](../../digital-portfolio-management/reference/dpm-landing.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Set up Service Owner Workspace](../image/SOWSetupBanner2.png "Navigate")

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Configuration** &gt; **Portfolio Metrics**.

2.  Click an existing service portfolio to learn what metrics are associated.

    The Portfolio Metrics list opens displaying all the metrics applied to the service portfolio.

3.  To add an additional metric to the service portfolio, click **New**.

4.  Fill in the form fields.

    |Field|Description|
    |-----|-----------|
    |Service portfolio|Select the service portfolio for which you want to create a metric|
    |Metric|Select the metric to apply. Choices include: **Activity**, **Availability**, **Breached SLA**, **Customer Satisfaction**, and **Critical Incidents**.|
    |Order|Specify the display order of the trend chart on the **Trends** tab in Service Owner Workspace.|
    |Trend chart|Check the box to display this metric on the **Trends** tab in Service Owner Workspace.|
    |Performance calculation|Check the box to use this metric in the service offering performance calculation.|

5.  Click **Submit**.

    For more information about Service Owner Workspace metrics and weight configuration, see [Service Owner Workspace performance metrics](../concept/understanding-SPM2-perform-metrics.md).


