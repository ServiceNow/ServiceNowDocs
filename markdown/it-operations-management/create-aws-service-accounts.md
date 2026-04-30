---
title: Create AWS service accounts
description: Create AWS service accounts on the ServiceNow AI Platform to access your AWS account during AWS discovery.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Setting up AWS service accounts, Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Create AWS service accounts

Create AWS service accounts on the ServiceNow AI Platform to access your AWS account during AWS discovery.

## Before you begin

-   Retrieve the user account number, which can be found in the AWS Management Console by expanding the list under the AWS account name.
-   Confirm that Discovery Admin Workspace is using at least version 1.10.0. The **Discovery** &gt; **Cloud Service Accounts** navigation module isn't available with earlier versions. To access **Cloud Service Accounts** with an earlier version, enter in the navigation filter: `cmdb_ci_cloud_service_account.list`.

Role required: discovery\_admin

## About this task

A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in cloud management of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts—even service accounts from different providers. For each service account, you specify which datacenter to include in the cloud account.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_f5b_r22_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The unique and meaningful name for this service account.

</td></tr><tr><td>

Account ID

</td><td>

12-digit user account number. Expand the list under the AWS account name on the AWS Management Console to view the number.**Important:** In the **Account ID** field, remove the hyphen characters \(-\) from the number.

 ![Determine the IAM user account number to fill in the Account ID field](../../cloud-management-v2-setup/image/aws-account-id.png "IAM user account number")

</td></tr><tr><td>

Discovery credentials

</td><td>

The credentials needed for ServiceNow applications to access this account. You may configure this field at a later stage, while configuring access to AWS accounts.

 -   If you [configured AWS credentials at ServiceNow AI Platform](aws-create-creds-cloud-mgt.md) , select the magnifying glass icon, and then select the name of the relevant AWS credential.
-   To use other AWS accounts to access this account, leave the field blank. For example, you don't need to specify the AWS credentials for accounts assuming IAM roles or member accounts using their management account for access.


</td></tr><tr><td>

Datacenter URL

</td><td>

URL of the datacenter.

 This field is required for AWS China region and AWS GovCloud \(US\) accounts.

 For example:

-   AWS China region: `https://organizations.cn-northwest-1.amazonaws.com.cn`
-   AWS GovCloud \(US\): `https://ec2.us-gov-west-1.amazonaws.com`


</td></tr><tr><td>

Datacenter type

</td><td>

Type of the datacenter where the account is hosted.Select **AWS datacenter**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Auto-generated value: Status and timestamp of the last execution of Discovery on the datacenter.

</td></tr><tr><td>

Parent account

</td><td>

Name of the management account that represents the organization in AWS that this member account belongs to.It appears when you select **AWS datacenter**.

 Leave the field empty if this account is not part of an AWS organization.

</td></tr><tr><td>

Is master account

</td><td>

Management account flag.It appears when you select **AWS datacenter** from the Datacenter Type drop-down. Select the check box to associate the AWS service account with the management account. Select this check box only for accounts that you previously configured in the AWS Management Console as management accounts with some member accounts belonging to them. See the [AWS documentation](https://aws.amazon.com/documentation/) for information on AWS Organizations.

**Note:** You will need to setup the correct permission in AWS or the Organization role for a standard credential. For more information, see [Control AWS access and permissions using policies](aws-create-user-policy-cloud-mgt.md).

</td></tr><tr><td>

Accessor account

</td><td>

Name of the trusted account. Configure this field only for accounts that don't use permanent AWS credentials and rely on IAM roles for access.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Setting up AWS service accounts](../concept/setup-aws-service-accounts.md)

