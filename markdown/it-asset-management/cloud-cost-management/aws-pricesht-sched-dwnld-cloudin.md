---
title: Schedule and manage the Cloud Cost Management jobs that download AWS price sheets
description: A Price Sheet Download job downloads and stores price sheet data. The Rightsizing and Unused resources processes use price sheet data when generating recommendations.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Cloud Cost Management for AWS, Configure, Cloud Cost Management, IT Asset Management]
---

# Schedule and manage the Cloud Cost Management jobs that download AWS price sheets

A Price Sheet Download job downloads and stores price sheet data. The Rightsizing and Unused resources processes use price sheet data when generating recommendations.

## Before you begin

For each provider, run Discovery on each service account.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\].

## About this task

-   You create a scheduled Price Sheet Download job for each provider.
-   Each execution of a Price Sheet Download job runs multiple execution items. Each execution item imports and stores the price sheet for one region.
-   To ensure accurate reporting and recommendations for some providers, make sure that the Discovery application runs before the scheduled execution.
-   When the scheduled time arrives, job execution happens in multiple stages \(for example, connect to the provider, download the data, perform the post-import sort, and so on\). The system logs status and results on the Price Sheet Executions page for each stage.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Price sheet download jobs**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="id_zd2_sct_zxb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Meaningful name for the Price Sheet Download job.

</td></tr><tr><td>

Provider

</td><td>

Name of the cloud provider.

</td></tr><tr><td>

Last successful execution

</td><td>

Timestamp of the most recent execution of the job.

</td></tr><tr><td>

Download Price Sheet For

</td><td>

Price sheet downloads for different services.-   AWS
    -   Compute and Storage
    -   Database
    -   All
-   Azure
    -   Compute
    -   Database
    -   Storage
-   Google
    -   Compute and Storage
    -   Database
    -   All


</td></tr><tr><td>

Active

</td><td>

Option for activating the Price Sheet Download Job. Only active jobs are executed.

</td></tr><tr><td>

Run

</td><td>

Frequency to execute the job.

 **Note:** Depending on the value that you select, additional fields appear. For example, if you select a **Run** value of **Monthly**, a **Day** field appears. A value of 3 would mean the third day of the month.

 This field is automatically set to **Monthly**.

</td></tr><tr><td>

Time

</td><td>

Time of day to execute the job.

</td></tr><tr><td>

Current execution status

</td><td>

Status of the execution that is currently running.

</td></tr><tr><td>

Current execution details

</td><td>

Details for the execution that is currently running.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  Select **Execute** to execute the job.

    During execution, Cloud Cost Management downloads and stores the data. You can find the execution ID, status, and execution logs in the **Price Sheet Executions** tab. If there’s no new data, the execution is marked **Skipped**. If the download process is stuck, the execution is marked as **Canceled**.


**Related topics**  


[Rightsizing resources](../concept/rs-cloudin.md)

[Specify rate discounts to enable accurate pricing for Rightsizing recommendations](discounts-specify-cloudin.md)

