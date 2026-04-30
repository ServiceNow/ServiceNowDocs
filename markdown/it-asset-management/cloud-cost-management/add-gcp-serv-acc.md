---
title: Add a Google Cloud service account
description: Add a Google Cloud service account to store the credential and access information.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Cloud Cost Management for Google Cloud, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Add a Google Cloud service account

Add a Google Cloud service account to store the credential and access information.

## Before you begin

Role required: sn\_cmp.cloud\_admin

Set up download jobs for billing and price sheet data for the service account.

## About this task

**Important:** This information applies to both the Cloud Cost Management and Cloud Insights Billing apps. All references to Cloud Cost Management also apply to Cloud Insights Billing.

A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Service accounts**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_pm4_gm2_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name for this service account.

</td></tr><tr><td>

Account Id

</td><td>

The project\_ID value from the associated JSON key file.

</td></tr><tr><td>

Discovery credentials

</td><td>

The credentials needed for ServiceNow applications to access this account. You may configure this field at a later stage, while configuring access to Google Cloud accounts.-   If you configured Google Cloud credentials at ServiceNow AI Platform, select the name of the relevant Google Cloud credential.
-   To use other Google Cloud accounts to access this account, leave the field empty.


</td></tr><tr><td>

Datacenter URL

</td><td>

URL of the datacenter.This field is required only for Google Gov Cloud accounts.

</td></tr><tr><td>

Datacenter Type

</td><td>

Type of the datacenter where the account is hosted.Select **Google Cloud Platform datacenter**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Status and timestamp of the last execution of Discovery on the datacenter.This value is generated automatically.

</td></tr><tr><td>

Is Billing Account

</td><td>

Option for enabling the account to access billing data.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The service account that you created gets listed on the **Service accounts** page.

**Related topics**  


[Schedule and manage the jobs that download Google Cloud billing data](gcp-bill-dwnld-job-cloudin.md)

[Schedule and manage the Cloud Cost Management jobs that download Google Cloud price sheets](gcp-pricesht-sched-dwnld-cloudin.md)

