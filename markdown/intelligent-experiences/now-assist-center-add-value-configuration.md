---
title: Add a value configuration in the Now Assist Center Business Value dashboard
description: Add a value configuration to define the business value metrics calculated for an AI asset, including average time saved per execution and average hourly rate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-center-add-value-configuration.html
release: zurich
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI, business value]
breadcrumb: [Now Assist Center Business Value, View AI assets usage and performance, Monitor, Now Assist Center, Enable AI experiences]
---

# Add a value configuration in the Now Assist Center Business Value dashboard

Add a value configuration to define the business value metrics calculated for an AI asset, including average time saved per execution and average hourly rate.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Value configurations define the data used to calculate business value metrics for each AI asset on the Business Value dashboard. Each configuration specifies the asset, average time saved per execution, and average hourly rate, which are used to calculate the total time saved and total cost saved displayed on the dashboard.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Center** or **Workspaces** &gt; **Now Assist Center**.

2.  Select **Business Value** in the top navigation bar.

3.  Select **Add configuration**.

    The **Add value configuration** modal opens.

4.  Select an **Asset type**.

5.  Select an **Asset name**.

    The **Execution count \(Last 7 days\)** field is automatically populated based on the selected asset's execution history and is read-only.

    The **Currency** field displays the currency configured for your instance. To change the currency, update your instance configuration.

6.  Enter a value in **Average time saved per execution \(min\)**.

7.  Enter a value in **Average hourly rate**.

    The **Total time saved \(hrs\)** and **Total cost saved** fields are calculated automatically based on the execution count, average time saved per execution, and average hourly rate values.

8.  Select **Add**.


## Result

A **Benchmark created successfully** confirmation banner appears. The value configuration is added to the **Business value configuration** table and the Business Value dashboard metrics are updated to reflect the new configuration.

**Parent Topic:**[Now Assist Center Business Value dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-business-value-dashboard.md)

