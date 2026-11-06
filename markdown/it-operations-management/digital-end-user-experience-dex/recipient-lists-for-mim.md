---
title: Customize recipient list for Major Incident Management updates
description: Customize the base system recipient list for Major Incident Management updates based on application usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/recipient-lists-for-mim.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [recipient lists, major incident management \(mim\), mim notifications, customize recipient list, targeted communications]
breadcrumb: [Administer, Digital End-User Experience, IT Operations Management]
---

# Customize recipient list for Major Incident Management updates

Customize the base system recipient list for Major Incident Management updates based on application usage.

## Before you begin

-   The DEX Score application must be installed.
-   Confirm that data is available in the DEX Score installed or web application tables.

    This data is tracked and used to filter the recipient list.

-   Verify that the DEX Score **Orchestrate generator aggregation** scheduled job is executed. This job runs daily to collect data.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Targeted Communications** &gt; **Recipients Lists**.

2.  Open the **Impacted application users in affected location\(s\)** recipient list.

3.  Edit the following details in the script:

<table id="table_z5k_bwb_glb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Aggregation Frequency

</td><td>

Frequency of data aggregation:-   Daily
-   Weekly
-   Monthly
By default, aggregation frequency is set to Daily.

</td></tr><tr><td>

Aggregation Period

</td><td>

Period of data aggregation:-   1–7 days
-   1–4 weeks
-   1–12 months
By default, aggregation period is set to 7 days.

</td></tr><tr><td>

Application type

</td><td>

Type of application used to filter users, either installed or web.

</td></tr><tr><td>

Application

</td><td>

The sys\_id of the application. For example, sys\_id of the Microsoft PowerPoint application.

</td></tr><tr><td>

Metric

</td><td>

Name of the metric. For example, Application Usage.

</td></tr><tr><td>

Metric value

</td><td>

Threshold value for the metric. The API filters users whose value for the selected metric is greater than this value.

</td></tr><tr><td>

Location id

</td><td>

The sys\_id of the location.

</td></tr></tbody>
</table>4.  Select **Update**.


