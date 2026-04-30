---
title: Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets
description: A Price Sheet Download job downloads and stores price sheet data. The Rightsizing and Unused resources processes use price sheet data when generating recommendations.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets

A Price Sheet Download job downloads and stores price sheet data. The Rightsizing and Unused resources processes use price sheet data when generating recommendations.

## Before you begin

Run the Discovery application on each service account.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\].

## About this task

-   You create a scheduled Price Sheet Download job for Microsoft Azure.
-   Each execution of a Price Sheet Download job runs multiple execution items. Each execution item imports and stores the price sheet for one subscription or billing profile.
-   To ensure accurate reporting and recommendations for some providers, make sure that Discovery runs before the scheduled execution.
-   When the scheduled time arrives, job execution happens in multiple stages \(for example, connect to the provider, download the data, perform the post-import sort, and so on\). The system logs status and results on the Price Sheet Executions page for each stage.
-   Cloud Cost Management version 9.0 supports price sheet download for both Azure Enterprise Agreement \(EA\) and Microsoft Customer Agreement \(MCA\) accounts.
-   Cloud Cost Management version 10.0 supports price sheet download for Microsoft Partner Agreement \(MPA\) accounts in addition to the Azure Enterprise Agreement \(EA\) and Microsoft Customer Agreement \(MCA\) accounts.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Price sheet download jobs**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_g3f_smc_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique and meaningful name for the Price Sheet Download job.

</td></tr><tr><td>

Provider

</td><td>

Name of the cloud provider.

</td></tr><tr><td>

Download retail price sheet

</td><td>

Option to download retail price sheet without the need to provide account details and credentials required for the download.

</td></tr><tr><td>

Azure Service Account

</td><td>

Name of the Azure service account.

</td></tr><tr><td>

Download Price Sheet For

</td><td>

Price sheet downloads for different services.-   Compute
-   Database
-   Storage


</td></tr><tr><td>

Last successful execution

</td><td>

Timestamp of the most recent execution of the job.

</td></tr><tr><td>

Active

</td><td>

Option for activating the Price Sheet Download Job. Only active jobs are executed.

</td></tr><tr><td>

Run

</td><td>

Frequency to execute the job. **Note:** Depending on the value that you select, additional fields appear. For example, if you select a **Run** value of **Monthly**, a **Day** field appears. A value of 3 would mean the third day of the month.

This field is automatically set to **Monthly**.

</td></tr><tr><td>

Time

</td><td>

Time of the day to execute the job.

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

