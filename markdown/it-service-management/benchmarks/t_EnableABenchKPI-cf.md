---
title: Enable a benchmark KPI
description: Enable KPIs to use in your data reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/benchmarks/t\_EnableABenchKPI-cf.html
release: xanadu
product: Benchmarks
classification: benchmarks
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Benchmarks, Benchmarks, IT Service Management]
---

# Enable a benchmark KPI

Enable KPIs to use in your data reporting.

## Before you begin

Role required:

The sn\_bm\_client.benchmark\_admin role can enable KPIs.

Admins can assign roles to a KPI category.

## About this task

KPIs are grouped within categories \(for example, ITSM, ITOM, Security Operations\). You can assign roles to certain categories so that the corresponding KPI data is limited to authorized groups.

## Procedure

1.  Navigate to **All** &gt; **Benchmarks** &gt; **Administration** &gt; **Setup**.

2.  To enable or disable a KPI, click the KPI slider.

3.  To view more information about a KPI, click the KPI.

    Additional information includes description, formula, conditions, and tables from which the data is collected.

4.  Click **Save**.

    Allow one to two months for aggregate monthly data to accurately reflect changes made to KPI status.

    **Note:** In some environments, resolved incident KPIs may require further configuration to retrieve resolved incident data.

5.  To limit access of benchmark data to specific categories, assign roles to a KPI category.

    1.  Navigate to **Benchmarks** &gt; **Administration** &gt; **Category** and select a KPI category.

    2.  To add a role, click **View Roles**.

        **Note:** You must have the admin role to assign roles to categories.


