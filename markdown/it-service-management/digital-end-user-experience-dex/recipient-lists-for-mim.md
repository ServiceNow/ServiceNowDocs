---
title: Update the recipient list for Major Incident Management updates based on application usage
description: Customize the attributes of the recipient list.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-04-02"
reading_time_minutes: 1
breadcrumb: [Desktop Assistant notifications, Desktop Assistant, Digital End-User Experience, IT Service Management]
---

# Update the recipient list for Major Incident Management updates based on application usage

Customize the attributes of the recipient list.

## About this task

You can edit the recipient list **All users based on the application usage in the affected location\(s\)**, which is provided by the DEX application with the base system. You can update the required attributes of the recipient list.

## Before you begin

-   Install the DEX Score application.
-   Have data available in the installed or web application tables in the DEX Score. This data is tracked based on which recipient list is filtered.
-   Verify that the Orchestrate Generator Aggregation scheduled job in DEX Score is run. This job runs daily and collects the data.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Targetted Communication** &gt; **Recipient list**.

2.  Open the **All users based on the application usage in the affected location\(s\)** recipient list.

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
.

</td></tr><tr><td>

Aggregation Period

</td><td>

Enter the aggregation period:-   1 to 7
-   1 to 4
-   1 to 12
.**Note:** By default, the aggregation frequency is set to daily, and the aggregation period is 7.

</td></tr><tr><td>

Application type

</td><td>

Enter either installed or web, based on this it filters the users.

</td></tr><tr><td>

Application

</td><td>

Enter a sys\_id of an application. For example, a sys\_id of the Microsoft PowerPoint application.

</td></tr><tr><td>

Metric

</td><td>

Enter a metric. For example, Application Usage.

</td></tr><tr><td>

Metric value

</td><td>

Enter a metric value. The API checks if the selected metric is greater than the metric value, based on this it filters the users.

</td></tr><tr><td>

Location id

</td><td>

Enter the sys\_id of the location.

</td></tr></tbody>
</table>4.  Select **Update**.


