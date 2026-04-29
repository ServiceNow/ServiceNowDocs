---
title: Add a Microsoft Azure service account
description: Add a Azure service account to store the credential and access information.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Add a Microsoft Azure service account

Add a Azure service account to store the credential and access information.

## Before you begin

Role required: sn\_cmp.cloud\_admin

Set up download jobs for billing and price sheet data for the service account.

## About this task

A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

**Note:** The service account must have Discovery credentials to get the Azure forecast data.

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

The Azure Account ID value that you copied from the Azure portal into the text file.The value in this field changes based on the type of account that you set.

-   For billing service accounts, the Account ID is the Enrollment ID.
-   For other service accounts, the Account ID is the Subscription ID.


</td></tr><tr><td>

Discovery credentials

</td><td>

The credentials needed for ServiceNow applications to access this account. You might configure this field at a later stage, while configuring access to Azure accounts.-   If you configured Azure credentials at ServiceNow AI Platform, select the name of the relevant Azure credential.
-   To use other Azure accounts to access this account, leave the field empty.


</td></tr><tr><td>

Datacenter URL

</td><td>

URL of the datacenter.This field is required only for Azure GovCloud \(US\) accounts.

.

</td></tr><tr><td>

Datacenter Type

</td><td>

Type of the datacenter where the account is hosted.Select **Azure datacenter**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Status and timestamp of the last execution of discovery on the datacenter.This value is generated automatically.

</td></tr><tr><td>

Is Billing Account

</td><td>

Option for enabling the account to access billing data.This option is available only when Cloud Integrations Azure scope is used.

For the existing billing accounts, this check box is selected by default.

</td></tr><tr><td>

Is Management Group

</td><td>

Option for enabling the account for running Discovery.This option is available only when Cloud Integrations Azure scope is used.

For the existing accounts where Discovery is run, this check box is selected by default.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The service account that you created gets listed on the **Service accounts** page.

**Related topics**  


[Schedule and manage the jobs that download Azure billing data](schedule-azure-billing-job.md)

[Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets](azure-pricesht-sched-dwnld-cloudin.md)

[Discovery for Microsoft Azure](https://www.servicenow.com/docs/access?context=azure-cloud-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

