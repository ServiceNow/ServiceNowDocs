---
title: Customize recipient list for Major Incident Management updates
description: Customize the base system recipient list for Major Incident Management updates based on application usage.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Notifications, Desktop Assistant, Digital End-User Experience, IT Service Management]
---

# Customize recipient list for Major Incident Management updates

Customize the base system recipient list for Major Incident Management updates based on application usage.

## Before you begin

-   Install the DEX Score application.
-   Confirm that data is available in the DEX Score installed or web application tables.

    This data is tracked and used to filter the recipient list.

-   Verify that the DEX Score **Orchestrate generator aggregation** scheduled job is executed. This job runs daily to collect data.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Targeted Communications** &gt; **Recipients Lists**.

2.  Open the **Impacted application users in affected location\(s\)** recipient list.

3.  Edit the following details in the script:

<table id="table_z5k_bwb_glb"><thead><tr><th>

Parameter list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Aggregation Frequency

</td><td>

Enter the aggregation frequency:-   Daily
-   Weekly
-   Monthly
By default, aggregation frequency is set to Daily.

</td></tr><tr><td>

Aggregation Period

</td><td>

Enter the aggregation period:-   1–7 days
-   1–4 weeks
-   1–12 months
By default, aggregation period is set to 7 days.

</td></tr><tr><td>

Application type

</td><td>

Enter application type as either installed or web, based on which users are filtered.

</td></tr><tr><td>

Application

</td><td>

Enter the sys\_id of an application. For example, sys\_id of the Microsoft PowerPoint application.

</td></tr><tr><td>

Metric

</td><td>

Enter a metric name. For example, Application Usage.

</td></tr><tr><td>

Metric value

</td><td>

Enter a metric value. The API checks if the selected metric is greater than the metric value, based on which it filters the users.

</td></tr><tr><td>

Location id

</td><td>

Enter the sys\_id of the location.

</td></tr></tbody>
</table>4.  Select **Update**.


