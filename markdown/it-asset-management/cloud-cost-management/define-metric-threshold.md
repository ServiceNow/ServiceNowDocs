---
title: Define a metric threshold
description: To enable accurate memory usage data for use in generating Rightsizing recommendations, you first define memory metrics in your account. You then define a custom memory metric in Cloud Cost Management.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Rightsizing operations, Resize resources with Rightsizing, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Define a metric threshold

To enable accurate memory usage data for use in generating Rightsizing recommendations, you first define memory metrics in your account. You then define a custom memory metric in Cloud Cost Management.

## Before you begin

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or insights\_owner \[sn\_clin\_core.insights\_owner\]

-   Run Discovery on each service account.
-   Verify that the Billing Download and Price Sheet Download job has been completed successfully.

## About this task

**Note:** You can configure the memory threshold for AWS and Azure only.

AWS doesn’t automatically collect memory metric statistics. On the AWS Management Console, you specify the statistics to collect and push the data to Amazon CloudWatch. Cloud Cost Management accesses the data through CloudWatch, and verifies that the combination of namespace and metric name is defined correctly. To recommend resources for Rightsizing, Cloud Cost Management analyzes the memory usage data for the custom metric. If no data is returned, the analysis uses the maximum memory of the resource.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Rightsizing**.

2.  Select **Settings**.

3.  Select the **Service category metric** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_iny_n51_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Name of the service provider.-   AWS
-   Azure


</td></tr><tr><td>

Service Category

</td><td>

Service category for the provider.-   Compute
-   Database
**Note:**

-   For AWS, recommendations are generated only on CPU usage \(Compute\).
-   For Azure, recommendations are generated based on CPU, Memory, and Network usage \(Compute and Database\).


</td></tr><tr><td>

Service Accounts

</td><td>

Service accounts for the selected provider.

</td></tr><tr><td>

Aggregation Type

</td><td>

Metric statistics received in time intervals.-   Avg
-   Min
-   Max


</td></tr><tr><td>

Metric Type

</td><td>

Type of the metric statistic.-   CPU
-   Memory
-   Network


</td></tr><tr><td>

Threshold \(%\)

</td><td>

Threshold value used while generating Rightsizing recommendations.**Note:** If **Provider** is selected as **AWS**, **Service Category**is selected as **Database**, and **Metric Type** is selected as **Network**, the value shows up as an integer.

</td></tr></tbody>
</table>6.  Select **Save**.


**Parent Topic:**[Configure Rightsizing operations](rs-settings-config-cloudin.md)

