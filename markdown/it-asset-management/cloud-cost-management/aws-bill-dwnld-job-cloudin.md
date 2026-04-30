---
title: Schedule and manage the jobs that download AWS billing data
description: Billing Download jobs download, organize, and store billing data for your payer account on the schedule that you specify. The system analyzes the data to generate reports and to make recommendations for changes in your cloud operations that can lead to cost savings.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 9
breadcrumb: [Set up access to AWS billing and usage data, Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Schedule and manage the jobs that download AWS billing data

Billing Download jobs download, organize, and store billing data for your payer account on the schedule that you specify. The system analyzes the data to generate reports and to make recommendations for changes in your cloud operations that can lead to cost savings.

## Before you begin

Role required: Cloud Integrations Admin \[sn\_cld\_intg\_core.cloud\_integrations\_admin\]

Ensure that your system has 8 GB Clotho memory and 4 GB mid memory.

Enable cost allocation for each Kubernetes cluster before you run an AWS Billing download job to view the Kubernetes spend. For more information, see [Enable cost allocation in AWS for Kubernetes cluster](enable-cost-allocation-aws.md).

## About this task

**Important:** This information applies to both the Cloud Cost Management and Cloud Insights Billing apps. All references to Cloud Cost Management also apply to Cloud Insights Billing.

During billing download, all the resources are pulled into the system. AWS Redshift resources are placed in the \[cmdb\_ci\_cloud\_database\] table. After the 4.0 upgrade, make sure that the billing download is executed with reimport true.

**Note:** From Cloud Cost Management version 8.1 onwards, the default time for billing download jobs has changed from 12:00 to 01:00 \(UTC\). Also, schedule or run Cloud Cost Management jobs only during off-business hours and when there's no other heavy operations or jobs running on the ServiceNow instance.

If you have installed the Cloud Cost Management Infra Stack application, then toward the end of a job, significant database update, and insert operations are performed based on your Cloud CIs and spend data volume. Thus, any other job that impacts database performance shouldn't be run during this time alongside Cloud Cost Management jobs.

-   Billing Download jobs can't be in the Global scope.
-   If the Cloud Provisioning and Governance application is installed on your instance: Both Cloud Provisioning and Governance and Cloud Cost Management download billing data. The two download jobs are separate processes and they don't interfere with each other.
-   You can create only one Billing Download job for each account \(enrollment\).
-   Configure AWS Billing download for the main account otherwise the spend doesn't generate.
-   To ensure accurate reporting and recommendations for some providers, make sure that Discovery runs before the scheduled execution.
-   Each successful execution of a Billing Download job triggers the Budget Forecast, Business hours, Reservation/saving plans, Rightsizing, and Unused resources jobs to analyze spend and usage data and to update the actionable recommendations in reports.
-   Each successful execution of a Billing Download job updates tagged costs. Recent updates that you make to tag category definitions \(for example, adding a tag name to a category\) might not be reflected in cost reports. To apply the latest tag category definitions to cost data without running a Billing Download job, select **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Cost usage tags** &gt; **Tag categories** and then select **Re-Apply Categories**.
-   When the scheduled time arrives, job execution happens in multiple stages \(for example, connect to the provider, download the data, perform the post-import sort, and so on\). The system logs status and results on the Price Sheet Executions page for each stage.
-   Cost categories are updated with new cost tag values each time billing data is downloaded. \(You define cost tags in the provider portal to associate usage data with a particular business entity. For example, the Cost Center category might include the tags `development`, `testing`, and `QA`. The User category might include the names of your users.\)
-   Billing data is downloaded in reverse chronological order by month. For example, if the range is from March to June, data for June is downloaded first.
-   To ensure meaningful results for the first billing data download, the app downloads data for at least 30 days. For example, if today is June 10 and you specify June for download, the system downloads data for both May and June to ensure at least 30 days of data for analysis.
-   You can download data only for the most recent twelve months.

For AWS.

-   You can create only one Billing Download job for each service account.
-   Only costs of the unblended type are supported.
-   The Billing Download job updates the billing node data table \[sn\_cld\_intg\_aws\_cost\_usage\] with the CIs in the CMDB that correspond to each resource ID.
-   The CI placement process associates downloaded cost and usage data with the appropriate CIs in the CMDB. See [Add an AWS CI class type to ensure accurate billing data](aws-class-type-add-cloudin.md) for the details.

## Procedure

1.  Review the settings to verify that the settings on the report meet the requirements for Cloud Cost Management when you have an existing AWS Cost and Usage Report \(CUR\).

2.  On the AWS Management Console, define an AWS CUR as follows:

    **Note:** You must configure Legacy CUR because Cloud Cost Management supports the legacy version only.

    1.  Follow the instructions in the [Creating Cost and Usage Reports](https://docs.aws.amazon.com/cur/latest/userguide/cur-create.html) topic and use the following settings:

        -   Select the **Include resource IDs** check box.
        -   Select the **Automatically refresh your Cost and Usage Report when** check box.
        -   Report path prefix: optional
        -   Set **Time granularity** to either **Daily** or **Hourly** as needed. The **Hourly** setting generates a larger, more granular data set.
        -   Set **Report versioning** to **Create new report version**.
        -   Set **Compression type** to **GZIP** or **ZIP**. Cloud Cost Management doesn’t support Parquet.
    2.  Track the following values because you enter them into a Cloud Cost Management form in a moment.

        -   Report name
        -   Report prefix
        -   Name of the S3 bucket that is the data storage area for the daily detailed billing records on the AWS account.
3.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Billing download jobs**.

4.  Select the **AWS** tab.

5.  Select **New**.

6.  On the form, fill in the fields:

<table id="table_qz2_sf1_yxb"><thead><tr><th>

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

The users or groups to be notified by email about the status of the job execution \(for example, download failure\). The system doesn’t send a notification for success.Users or groups with the Cloud Integrations Admin \[sn\_cld\_intg\_core.cloud\_integrations\_admin\] role are well suited to handle these issues.

To update the email template, navigate to **System Notification** &gt; **Email** &gt; **Notifications** and open the Notify on billing job execution error template. For information on configuring the email, see [Create an email template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailTemplate&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Active

</td><td>

Option for activating the job. Only active jobs are executed.

</td></tr><tr><td>

Run

</td><td>

Frequency with which to execute the Billing Download job.**Note:**

-   For AWS, Billing Download jobs collect data once per day, even if AWS collects hourly usage data.
-   Depending on the value that you select, additional fields appear.
This field is automatically set to **Daily**.

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

AWS Settings

</td></tr><tr><td>

Service account

</td><td>

The AWS service account.

</td></tr><tr><td>

Bucket

</td><td>

Amazon S3 bucket that is the data storage area for the detailed hourly billing records on the AWS account.

</td></tr><tr><td>

Report name

</td><td>

The report-name value that appears in your AWS Cost and Usage Report.

</td></tr><tr><td>

Report prefix

</td><td>

The `report-prefix` value that appears in your AWS Cost and Usage Report.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  On the **Billing download jobs** page, select the created job.

9.  Select **Test connection**.

    The Test Connection workflow uses the settings that you configured to attempt to access the provider account. The system displays a progress pop-up and a success/error message that suggests actions to fix the configured settings.

10. Select **Execute now** to execute the job after the connection succeeds.

11. In the **Download billing data** dialog box, fill in the fields.

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
</table>12. Select **Download**.

    An AWS billing download job goes through the following states during the job execution:

    1.  **Ready**: The job is in the queue. For example, when a job is created to download billing data for a few months, the jobs for all months except the latest month are in Ready state.
    2.  **Requested**: The job is fetched and processed immediately. For example, the job that's created to download billing data for a month is in the Requested state. Also, when a job is created to download billing data for more than a month, the latest month job is also in the Requested state.

        **Note:** If you have installed the Cloud Cost Management Infra Stack application, it takes some time for the job to change from Ready to Requested state for AWS billing download job with Assume role authentication. This is because it takes time for the files to be downloaded to Cloud Cost Management MID Server. For details, see [Processing AWS billing jobs with Assume role authentication](../concept/process-aws-assume-infra.md).

    3.  **Reserved**: Job is picked by the Kubernetes cluster for processing. The Kubernetes cluster also sends the Job Id to Cloud Cost Management Glide to show which Kubernetes job is processing the billing job.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    4.  **In Progress**: Billing data is being processed.
    5.  **Sink Begin**: Kubernetes cluster sends some part of the processed billing data to the tables such as Spend Report Daily Aggregate Cost and Spend Report Monthly Aggregate Cost on Cloud Cost Management Glide. The records in these tables are in the Generating state. The job remains in the Sink Begin state until the entire billing data is sent to Cloud Cost Management Glide.

        In the Sink Begin state, the CI placement also starts and the Status of the CI Placement Stage changes from Ready to In Progress.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    6.  **Sink Complete**: All the processed billing data is sent to Cloud Cost Management Glide from the Kubernetes cluster.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    7.  **Finished**: Status after Sink Complete when all the billing files are sent to the Glide database.

        **Note:** The following changes happen when the job is marked Finished:

        -   The state of the records in the Spend Report Daily Aggregate Cost and Spend Report Monthly Aggregate Cost tables change from Generating to Active. Also, existing records are marked inactive.
        -   The billing account for which the billing file was downloaded is automatically set as a Master account in the Service Accounts table.
    8.  **Success**: Job is completed successfully.

## Result

The following events happen when the job executes:

-   While downloading the data, Cloud Cost Management updates the billing node data table \[sn\_cld\_intg\_&lt;provider&gt;\_cost\_usage\] with the CIs in the CMDB that correspond to each resource ID. If a CI doesn’t exist, the system generates a placeholder CI. On subsequent discovery, the system reconciles the placeholder CI.
-   Cloud Cost Management generates a log entry for each stage of the execution on the Billing Download Executions page.

