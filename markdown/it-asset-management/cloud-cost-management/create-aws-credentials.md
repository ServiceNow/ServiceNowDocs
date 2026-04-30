---
title: Create AWS credentials
description: Create credentials in the AWS Management Console to specify the credentials of the user when you configure the MID Servers that communicate with your AWS account.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up access to AWS billing and usage data, Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Create AWS credentials

Create credentials in the AWS Management Console to specify the credentials of the user when you configure the MID Servers that communicate with your AWS account.

## Before you begin

Role required: AWS Management Console administrator

You should be familiar with AWS policies. If you use IAM, you must know how to create an IAM user and set up a user policy. For more information about IAM, see [AWS documentation](https://docs.aws.amazon.com/).

## Procedure

1.  On the AWS Management Console, enter IAM in the AWS services search box to open the Identity and Access Managements \(IAM\) service.

2.  On the IAM Resources portal, select **Users**.

3.  Select **Add user**.

4.  On the Details page, configure the user settings as shown and then select **Next**.

    |Field|Value|
    |-----|-----|
    |User name|Name for the programmatic user, for example, `servicenowcloud`.|
    |Access type|`Programmatic access`.|

5.  On the Permissions page, configure the following settings and then select **Next**.

<table id="table_kpf_bng_rzb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Set permissions for &lt;username&gt;

</td><td>

Attach existing policies directly.

</td></tr><tr><td>

Attach one or more policies

</td><td>

The appropriate policy.**Note:** The AdministratorAccess policy has the most powerful permission level, including permission to provision cloud resources.

You might instead prefer to create a policy or combine multiple policies to grant the appropriate permission level. For more information, see [Create an AWS IAM user policy for Cloud Cost Management](aws-user-policy-create-cloudin.md).

</td></tr></tbody>
</table>6.  On the Review page, verify your selections and then select **Create user**.

7.  On the Complete page, select **Download .csv** to save a CSV backup file that contains the username, Access key ID, and the Secret access key value.

    You can create the file as a backup in case that you lose those values. Verify that the file was created and then store the file securely.


## What to do next

Create a record of the AWS credentials in Cloud Cost Management.

