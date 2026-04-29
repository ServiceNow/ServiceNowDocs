---
title: Schedule and manage the jobs that download Azure billing data
description: Billing Download jobs download, organize, and store billing data for your payer account on the schedule that you specify. The system analyzes the data to generate reports and to make recommendations for changes in your cloud operations that can lead to cost savings.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Schedule and manage the jobs that download Azure billing data

Billing Download jobs download, organize, and store billing data for your payer account on the schedule that you specify. The system analyzes the data to generate reports and to make recommendations for changes in your cloud operations that can lead to cost savings.

## Before you begin

Ensure that your system has 8 GB Clotho memory and 4 GB mid memory.

Role required: Cloud Integrations Admin \[sn\_cld\_intg\_core.cloud\_integrations\_admin\]

## About this task

-   To ensure accurate reporting and recommendations for some providers, make sure that Discovery runs before the scheduled execution.
-   You can create only one Billing Download job for each service account.
-   Only costs of unblended type are supported.
-   Each successful execution of a Billing Download job updates tagged costs. Recent updates that you make to tag category definitions \(for example, adding a tag name to a category\) might not be reflected in cost reports. You should map tag values to tag categories after the first run because populating tag values needs at least one successful run. For more information on applying the latest tag category definitions to cost data without running a Billing Download job, see [Create and update a tag category](tag-category-crud-cloudin.md).
-   When a Billing Download job successfully completes, it triggers the Budget Forecast, Business hours, Reservation/saving plans, Rightsizing, and Unused resources jobs to analyze spend and usage data. This action also updates the actionable recommendations in reports.
-   When the scheduled time arrives, job execution happens in multiple stages \(for example, connect to the provider, download the data, perform the post-import sort, and so on\). The system logs status and results on the Price Sheet Executions page for each stage.
-   Cost categories are updated with new cost tag values each time billing data is downloaded. For example, the Cost Center category might include the tags development, testing, and QA. The User category might include the names of your users.
-   Billing data is downloaded in reverse chronological order by month. For example, if the range is from March to June, data for June is downloaded first.
-   To ensure meaningful results for the first billing data download, the app downloads data for minimum 30 days. For example, if today is June 10 and you specify June for download, the system downloads data for both May and June to ensure a minimum 30 days of data for analysis.
-   You can download data only for the most recent 12 months.
-   Whenever you provision a Kubernetes cluster, one default resource group gets created as **MC\_myResourceGroup\_myAKSCluster\_eastus**. For example, if you provision a Kubernetes cluster with a resource group name as **TestResourceGroup**, Azure uses this resource group name and provisions another resource group as **MC\_&lt;name of the resource group&gt;\_&lt;name of the cluster&gt;\_&lt;location of the cluster&gt;**.

    All resources of the Kubernetes cluster are included in the resource group provided by Azure. When you run a Billing Download job, the list of resources included in the resource group with this naming convention **MC\_&lt;name of the resource group&gt;\_&lt;name of the cluster&gt;\_&lt;location of the cluster&gt;** is checked.

    -   A tag **sn\_ccm\_k8\_cluster\_name** is added to the Kubernetes cluster when the billing download job runs.
    -   A tag **sn\_ccm\_k8\_cluster\_name** is added to the resources of the Kubernetes cluster present in the resource group when the Spend job runs.
    **Note:**

    -   If you provide your own name to the asset or resources of a resource group, you can't view the spend for Kubernetes clusters.
    -   Install Discovery and Service Mapping Patterns application \(sn\_itom\_pattern\) 1.10.2 or higher. For more information, see [Install Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=install-discovery-service-mapping-patterns&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
    -   Install CMDB CI Class Models \(sn\_cmdb\_ci\_class\) version 1.53.1 or higher. For more information, see [CMDB CI Class Models app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
    -   To set up Kubernetes discovery, see [Kubernetes discovery using patterns](https://www.servicenow.com/docs/access?context=kubernetes-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   If you have installed the Cloud Cost Management Infra Stack application along with Cloud Cost Management version 8.1, bill processing only happens on the Kubernetes cluster outside the Glide but within the ServiceNow datacenter. This framework supports parallel processing of data in chunks, making the billing file download faster.

    After you submit a request for Azure billing data, the blobs are generated based on the chunk size. You can use the system property **sn\_cld\_intg\_azure.billing\_chunk\_duration** to set the chunk size. For details, see [Configure the chunk size of Microsoft Azure billing blob](config-aws-blob-ccminfra.md). Consider an example where you want to download 30 days of billing data and you have set the chunk size to 3, then the billing data is available in 10 blobs. After all the blobs are generated, the state of the job changes from Ready to Requested. These blobs are stored in some blob storage on the Azure portal. The Kubernetes framework then downloads and processes the generated blobs from Azure.

    **Note:**

    If you have installed the Cloud Cost Management Infra Stack application, then toward the end of a job, significant database update, and insert operations are performed based on your Cloud CIs and spend data volume. Thus, any other job that impacts database performance shouldn't be run during this time alongside Cloud Cost Management jobs.

-   From Cloud Cost Management version 8.1 onwards, the default time for billing download jobs has changed from 12:00 to 01:00 \(UTC\). Also, schedule or run Cloud Cost Management jobs only during off-business hours and when there's no other heavy operations or jobs running on the ServiceNow instance.
-   Cloud Cost Management version 10.0 and later versions support the FinOps Open Cost and Usage Specification \(FOCUS\), the industry standard for delivering billing and usage data.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Billing download jobs**.

2.  Select the **Azure** tab.

3.  Select **New**.

4.  On the form, fill in the fields:

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

The users or groups to be notified by email of the status of the job execution \(for example, download failure\). The system doesn’t send a notification for success.Users or groups with the Cloud Integrations Admin \[sn\_cld\_intg\_core.cloud\_integrations\_admin\] role are well suited to handle these issues.

To update the email template, navigate to **System Notification** &gt; **Email** &gt; **Notifications** and open the Notify on billing job execution error template. For information on configuring the email, see [Create an email template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailTemplate&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

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

Azure Settings

</td></tr><tr><td>

Azure Service account

</td><td>

The Azure service account.

</td></tr><tr><td>

Use Exports

</td><td>

Option for selecting the Azure Export method.The **Use Exports** check box is selected by default. If you don't want to use the Exports method, you must clear this check box.

</td></tr><tr><td colspan="2">

The following fields appear when the **Use Exports** check box is selected.

</td></tr><tr><td>

Billing Account Id Type

</td><td>

Level of billing account ID.Values include:

-   Account: When the billing is done on account level
-   Subscription: When the billing is done on subscription level
**Note:** Select **Account** when the account ID is selected in the **Azure Service Account** field.

</td></tr><tr><td>

Billing format

</td><td>

The type of billing format.Values include:

-   Cloud Native
-   Focus


</td></tr><tr><td colspan="2">

The following fields are visible when you select **Cloud Native** in the **Billing format** field.

</td></tr><tr><td>

Actual Cost Export Name

</td><td>

Name of the actual cost export configured on the Azure portal.For more information, see [Create exports on the Azure portal](create-azure-exports.md).

</td></tr><tr><td>

Amortized Cost Export Name

</td><td>

Name of the amortized cost export configured on the Azure portal.For more information, see [Create exports on the Azure portal](create-azure-exports.md).

</td></tr><tr><td colspan="2">

The following field is visible when you select **Focus** in the **Billing format** field.

</td></tr><tr><td>

Focus Export Name

</td><td>

Name of the export as configured for the FOCUS billing format.

</td></tr></tbody>
</table>    ![Azure Settings section on the Azure Billing Download Job form](../image/azure-exports.png)

5.  Select **Save**.

6.  On the **Billing download jobs** page, select the created job.

7.  Select **Test connection**.

    The Test Connection workflow uses the settings that you configured to attempt to access the provider account. The system displays a progress pop-up and a success/error message that suggests actions to fix the configured settings.

8.  Select **Execute now** to execute the job after the connection succeeds.

9.  In the **Download billing data** dialog box, fill in the fields.

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

Option for overwriting data from an earlier download attempt.**Note:**

The complete billing download occurs on the fourth day or on the billing finalization date for the previous month, irrespective of the Re-import data option setting.

</td></tr></tbody>
</table>10. Select **Download**.

    An Azure billing download job goes through the following states during the job execution:

    1.  **Ready**: Job is in the queue. For example, when a job is created to download billing data for a few months, the jobs for all months except the latest month are in Ready state.

        **Note:** If you have installed the Cloud Cost Management Infra Stack application, the Azure blob URLs are generated in the Ready state. For details, see [Configure the chunk size of Microsoft Azure billing blob](config-aws-blob-ccminfra.md). Only when all the blobs are generated, the state changes to Requested.

    2.  **Requested**: Job is fetched immediately. For example, the job that's created to download billing data for a month is in the Requested state. Also, when a job is created to download billing data for more than a month, the latest month job is also in the Requested state.
    3.  **Reserved**: Job is picked by the Kubernetes cluster for processing. The Kubernetes cluster also sends the Job Id to the Glide side to show which Kubernetes job is processing the billing job.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    4.  **In Progress**: Billing data is being processed.
    5.  **Sink Begin**: Kubernetes cluster sends some part of the processed billing data to the tables such as Spend Report Daily Aggregate Cost and Spend Report Monthly Aggregate Cost on the Glide. The records in these tables are in the Generating state. The job remains in the Sink Begin state until the entire billing data is sent to Cloud Cost Management Glide.

        In the Sink Begin state, the CI placement also starts and the Status of the CI Placement Stage changes from Ready to In Progress.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    6.  **Sink Complete**: All the processed billing data is sent to Cloud Cost Management Glide from the Kubernetes cluster.

        **Important:** This state is applicable only if you have installed the Cloud Cost Management Infra Stack application.

    7.  **Finished**: Status after Sink Complete when all the billing files are sent to the Glide database.

        **Note:** The following changes happen when the job is marked Finished:

        -   The state of the records in the Spend Report Daily Aggregate Cost and Spend Report Monthly Aggregate Cost tables change from Generating to Active. Also, existing records are marked inactive.
        -   The status of the Azure EA to SA mapping execution stage changes from Ready to In Progress. In this execution stage, the Enterprise account is mapped to the Service account.
    8.  **Success**: Job is completed successfully.

## Result

The following events happen when the job executes:

-   While downloading the data, Cloud Cost Management updates the billing node data table \[sn\_cld\_intg\_&lt;provider&gt;\_cost\_usage\] with the CIs in the CMDB that corresponds to each resource ID. If a CI doesn’t exist, the system generates a placeholder CI. On subsequent discovery, the system reconciles the placeholder CI.
-   Cloud Cost Management generates a log entry for each stage of the execution on the Billing Download Executions page.

**Note:** The supported CIs are placed after the Cumulus Unsupported CI Placement scheduled job runs daily. For more information, see [Supported CI class types for Microsoft Azure services](../reference/azure-supported-ci-class-types.md).

