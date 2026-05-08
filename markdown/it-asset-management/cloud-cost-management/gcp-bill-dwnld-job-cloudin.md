---
title: Schedule and manage the jobs that download Google Cloud billing data
description: Billing Download jobs download, organize, and store billing data for your payer account on the schedule that you specify. The system analyzes the data to generate reports and to make recommendations for changes in your cloud operations that can lead to cost savings.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Set up access to Google Cloud billing and usage data, Configure Cloud Cost Management for Google Cloud, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Schedule and manage the jobs that download Google Cloud billing data

Billing Download jobs download, organize, and store billing data for your payer account on the schedule that you specify. The system analyzes the data to generate reports and to make recommendations for changes in your cloud operations that can lead to cost savings.

## Before you begin

-   Ensure that your system has 8 GB Clotho memory and 4 GB mid memory.
-   You must set up required roles to perform billing download. For more information, see [Setup roles for Google Cloud billing download](gcp-user-policy-create-cloudin.md).
-   Enable cost allocation for each Kubernetes cluster before you run a Google Cloud Billing download job to view the Kubernetes spend. For more information, see [Enable cost allocation in Google Cloud for Kubernetes cluster](enable-cost-allocation-kc-gcp.md).

Roles required:

-   On the Google Cloud Console: Google Cloud administrator.
-   Cloud Cost Management: insights\_admin \[sn\_clin\_core.insights\_admin\] or admin.

## About this task

During the billing download, all the resources are pulled into the system. GCP SQL databases are placed in the \[cmdb\_ci\] table.

**Note:** From Cloud Cost Management version 8.1 onwards, the default time for billing download jobs has changed from 12 a.m. to 1 a.m. \(UTC\). Also, schedule or run Cloud Cost Management jobs only during off-business hours and when there's no other heavy operations or jobs running on the ServiceNow instance.

If you have installed the Cloud Cost Management Infra Stack application, then toward the end of a job, significant database update, and insert operations are performed based on your Cloud CIs and spend data volume. Thus, any other job that impacts database performance shouldn't be run during this time alongside Cloud Cost Management jobs.

-   A Billing Download job creates and updates the billing node data table \[sn\_cld\_intg\_gcp\_cost\_usage\] with billing line items from the BigQuery dataset.

    **Note:** Charges associated with BigQuery usage are based on billing plans.

-   The CI placement process associates downloaded cost and usage data with the appropriate CIs in the CMDB. See [Add a Google Cloud CI class type to ensure accurate billing data](gcp-class-type-add-cloudin.md) for details.
-   Billing Download jobs can’t be in the Global scope.
-   You can create only one Billing Download job for each account.
-   To ensure accurate reporting and recommendations for some providers, make sure that the Discovery application runs before the scheduled execution.
-   Each successful execution of a Billing Download job triggers the Budget Forecast, Business hours, Reservation/saving plans, Rightsizing, and Unused resources jobs to analyze spend and usage data and to update the actionable recommendations in reports.
-   Each successful execution of a Billing Download job updates tagged costs. Recent updates that you make to tag category definitions \(for example, adding a tag name to a category\) might not be reflected in cost reports. You should map tag values to tag categories after the first run because populating tag values needs at least one successful run. You can apply the latest tag category definitions to cost data without running a Billing Download job, by selecting **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Cost usage tags** &gt; **Tag categories** and then selecting **Re-Apply Categories**.
-   When the scheduled time arrives, job execution happens in multiple stages \(for example, connect to the provider, download the data, perform the post-import sort, and so on\). The system logs status and results on the Price Sheet Executions page for each stage.
-   Cost categories are updated with new cost tag values each time billing data is downloaded. \(You define cost tags in the provider portal to associate usage data with a particular business entity. For example, the Cost Center category might include the tags `development`, `testing`, and `QA`. The User category might include the names of your users.\)
-   Billing data is downloaded in reverse chronological order by month. For example, if the range is from March to June, data for June is downloaded first.
-   To ensure meaningful results for the first billing data download, the app downloads data for at least 30 days. For example, if today is June 10 and you specify June for download, the system downloads data for both May and June to ensure at least 30 days of data for analysis.
-   You can download data only for the most recent twelve months.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Billing download jobs**.

2.  Select the **Google** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_x3f_2fg_yxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Meaningful name for the scheduled execution of the Billing Download job.

</td></tr><tr><td>

Last successful execution

</td><td>

The timestamp of the most recent successful execution.

</td></tr><tr><td>

Notify users/groups

</td><td>

The users or groups to notify by email of the status of the job execution \(for example, download failure\). The system doesn’t send a notification for success.Users or groups with the Cloud Integrations Admin \[sn\_cld\_intg\_core.cloud\_integrations\_admin\] role are well suited to handle these issues.

To update the email template, navigate to **System Notification** &gt; **Email** &gt; **Notifications** and open the Notify on billing job execution error template. For information on configuring the email, see Create an email template.

</td></tr><tr><td>

Active

</td><td>

Option for activating the job. Only active jobs are executed.

</td></tr><tr><td>

Run

</td><td>

Frequency with which to execute the Billing Download job.This field is automatically set to **Daily**.

**Note:** Depending on the value that you select, additional fields appear.

</td></tr><tr><td>

Time

</td><td>

Time of day to execute the job.

</td></tr><tr><td>

Latest execution status

</td><td>

The status of the most recently executed job.

</td></tr><tr><td>

Latest execution details

</td><td>

Execution details of the most recently executed job.

</td></tr><tr class="sub-head"><td colspan="2">

Google Settings

</td></tr><tr><td>

Billing account

</td><td>

Account to access for billing data. Every account for which the **Is Billing account** setting is true appears in the selection list. For more information about the **Is Billing account** field, see [Add a Google Cloud service account](add-gcp-serv-acc.md).For example, the Billing account ID must be in the `0XX0A-AXX9-6XXXA` format.

</td></tr><tr><td>

BigQuery project Id

</td><td>

The project ID, which contains the BigQuery dataset.

</td></tr><tr><td>

BigQuery dataset name

</td><td>

The name of the BigQuery dataset where the billing data is getting stored on an hourly basis.

</td></tr></tbody>
</table>5.  Select **Test Connection**.

    The Test Connection workflow uses the settings that you configured to attempt to access the provider account. The system displays a progress pop-up and a success/error message that suggests actions to fix the configured settings.

6.  Select **Execute now** to execute the job after the connection succeeds.

7.  In the **Download billing data** dialog box, fill in the fields.

<table id="table_gnf_11y_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start month

</td><td>

Starting month for downloading the billing data.**Note:** Data is downloaded for the specified months. If fewer than 30 days of data for analysis is received, data for the preceding month is also downloaded.

</td></tr><tr><td>

End month

</td><td>

Ending month for downloading the billing data.

</td></tr><tr><td>

Re-import data

</td><td>

Option for overwriting data from an earlier download attempt.

</td></tr></tbody>
</table>8.  Select **Download**.

    A Google Cloud billing download job goes through the following states during the job execution:

    1.  **Ready**: Job is in queue. For example, when a job is created to download billing data for a few months, the jobs for all months except the latest month are in Ready state.
    2.  **Requested**: Job will be fetched and processed immediately. For example, the job that's created to download billing data for a month is in the Requested state. Also, when a job is created to download billing data for more than a month, the latest month job is also in the Requested state.
    3.  **Reserved**: Job is picked by the Kubernetes cluster for processing. The Kubernetes cluster also sends the Job Id to Cloud Cost Management Glide to show which Kubernetes job is processing the billing job.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    4.  **In Progress**: Billing data is being processed.
    5.  **Sink Begin**: Kubernetes cluster sends some part of the processed billing data to the tables such as Spend Report Daily Aggregate Cost and Spend Report Monthly Aggregate Cost on the Glide. The records in these tables are in the Generating state. The job remains in the Sink Begin state until the entire billing data is sent to Glide.

        In the Sink Begin state, the CI placement also starts and the Status of the CI Placement Stage changes from Ready to In progress.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    6.  **Sink Complete**: All the processed billing data is sent to Cloud Cost Management Glide from the Kubernetes cluster.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    7.  **Finished**: Status after Sink Complete when all the billing files are sent to the Glide database.

        **Note:** The following changes happen when the job is marked Finished:

        -   The state of the records in the Spend Report Daily Aggregate Cost and Spend Report Monthly Aggregate Cost tables change from Generating to Active. Also, existing records are marked inactive.
        -   All the sub accounts are mapped to the parent account.
    8.  **Success**: Job is completed successfully.

## Result

The following events happen when the job executes:

-   While downloading the data, Cloud Cost Management updates the billing node data table \[sn\_cld\_intg\_&lt;provider&gt;\_cost\_usage\] with the CIs in the CMDB that correspond to each resource ID. If a CI doesn’t exist, the system generates a placeholder CI. On subsequent discovery, the system reconciles the placeholder CI.
-   Cloud Cost Management generates a log entry for each stage of the execution on the Billing Download Executions page.

