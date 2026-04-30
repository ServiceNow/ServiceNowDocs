---
title: Define the schedule for downloading AWS billing data
description: Define the scheduled job that regularly uses a MID Server to download billing data from the provider. Cloud Provisioning and Governance saves the data in a cost table and uses the information to generate reports.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Define the schedule for downloading AWS billing data

Define the scheduled job that regularly uses a MID Server to download billing data from the provider. Cloud Provisioning and Governance saves the data in a cost table and uses the information to generate reports.

## Before you begin

**Important:**

Starting with the Vancouver release, the Billing dashboard is no longer available if you have downloaded and activated the ServiceNow Store Cloud Cost Management app. The following changes occur:

-   You are redirected to the Cloud Cost Management home page by default.
-   The View Dashboard widget in the Cloud User portal is replaced by the View Resources widget.
-   The Current Month Spend widget and the Budget widget on the Cloud User portal do not show any data if Cloud Cost Management is activated on the instance.

If you have activated the Cloud Cost Management app, you can only navigate to the Billing Dashboard, if you are using Cloud Provisioning and Governance on a domain separated instance.

-   Set up a payer account that gets billing information for all linked accounts.
-   Create the Amazon S3 bucket that is the data storage area for the daily detailed billing records on the AWS account. The credential that is used to access the report must have permissions to the S3 bucket. Set the S3 bucket based on the Order location. The `AssumeRole` policies MUST include an S3 access policy. You might assume that the AWS account that you always use can create an S3 bucket in the region where the CFT is being provisioned. If you use STS-based authentication, however, the AWS account might not be able to create the bucket because authentication is tied to the `AssumeRole` policies. See the "Setting Up an Amazon S3 Bucket for AWS Cost and Usage Reports" page in the [AWS documentation](https://aws.amazon.com/documentation/) for details.
-   Enable detailed billing reports on AWS. See the [AWS documentation](https://aws.amazon.com/documentation/) for details.

    **Note:** The Detailed Billing Report feature is withdrawn by Amazon AWS Cloud for new customers. For more information, and for migration details see the AWS documentation on [Detailed Billing Reports](https://docs.aws.amazon.com/cur/latest/userguide/detailed-billing.html).


Role required: sn\_cmp.cloud\_governor

## About this task

This procedure involves two tasks:

1.  Fill in the AWS Billing Schedule form with information that you copy from the AWS portal. This action enables the instance to download AWS billing data.
2.  Specify the schedule for downloading AWS billing information.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Analyze** &gt; **Billing**.

2.  On the **Billing Schedules** tab, click **New**, enter a unique and meaningful **Name**, and then fill in the form.

<table id="table_h12_rly_my"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Select **AWS**.

</td></tr><tr><td>

Service Account

</td><td>

The AWS service account that you created during initial setup. \(The AWS account to run the billing report on.\)

</td></tr><tr><td>

Bucket

</td><td>

Data storage area for the daily billing records on the AWS account. Follow this procedure to obtain the value:1.  Log in to the AWS Management Console and select **My Billing Dashboard** in the menu.
2.  From the dashboard, select **Billing Preferences**.
3.  In the **Cost Management Preferences**section, expand **Detailed Billing Reports \[Legacy\]** and ensure that the **Turn on the legacy Detailed Billing Reports feature to receive ongoing reports of your AWS charges** check box is selected.
4.  Copy the value from the **Save the S3 bucket:** field into the **Bucket** field on the form.

**Note:** By default, AWS selects the S3 bucket associated with the AWS account that you are currently signed into. A green tick indicates that the bucket is configured correctly.

</td></tr><tr><td>

Active

</td><td>

Select the check box to activate the download job.

</td></tr><tr><td>

Run

</td><td>

Frequency that the download job should run.

</td></tr><tr><td>

Time

</td><td>

Time of day that the download job should run.

</td></tr></tbody>
</table>3.  Click **Save**.

    To run the schedule on demand, click **Execute Now**. On the **Retrieve Billing Data** window that appears, select a date range and then click **Download**.


## What to do next

[View cloud costs on the Billing dashboard](../../cloud-management-v2/concept/cloud-dashboards.md#).

**Related topics**  


[Cloud credentials](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

