---
title: Add an AWS GovCloud service account
description: If your organization uses AWS GovCloud \(US\) regions, you create a service account for each region. The credentials that you create during the service account creation, are used for Cloud Discovery and Cloud Cost Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/aws-gov-service-acct-add-cloudin.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Add an AWS GovCloud service account

If your organization uses AWS GovCloud \(US\) regions, you create a service account for each region. The credentials that you create during the service account creation, are used for Cloud Discovery and Cloud Cost Management.

## Before you begin

Role required: sn\_cmp.cloud\_admin

-   AWS GovCloud \(US\) credentials for each GovCloud region.
-   AWS GovCloud \(US\) account ID \(from the AWS Management Console\).

## About this task

A service account holds the credential and account information that you created in your provider account. A cloud\_admin can add an AWS GovCloud service account. Be sure to set up download jobs for billing and price sheet data for the service account.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Service accounts**.

2.  Select **New**.

3.  On the Cloud Service Account form, fill in the fields.

<table id="table_dcn_smd_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique and descriptive name for the service account. For example, `AWS GovCloud SA 01`.

</td></tr><tr><td>

Account Id

</td><td>

Account ID to which this credential belongs.

</td></tr><tr><td>

Discovery credentials

</td><td>

Name of the credentials that you created in the [Create an AWS IAM user policy for Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-user-policy-create-cloudin.md) procedure.

</td></tr><tr><td>

Datacenter URL

</td><td>

URL of the datacenter. For example, [https://ec2.us-gov-west-1.amazonaws.com](https://ec2.us-gov-west-1.amazonaws.com/)

</td></tr><tr><td>

Datacenter Type

</td><td>

Type of the datacenter where the account is hosted.Select **AWS datacenter**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Status and timestamp of the last execution of the Discovery application on the datacenter.

</td></tr><tr><td>

Is Billing Account

</td><td>

The option for enabling the account to access billing data.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

The service account gets created and displays the list of all discovered datacenters.

**Related topics**  


[Schedule and manage the jobs that download AWS billing data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-bill-dwnld-job-cloudin.md)

[Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-pricesht-sched-dwnld-cloudin.md)

