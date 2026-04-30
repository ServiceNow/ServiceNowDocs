---
title: Configure the MID Server for AWS IAM roles
description: Configure the MID Server to retrieve the temporary security credentials associated with an IAM role.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up AWS service accounts, Setting up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Configure the MID Server for AWS IAM roles

Configure the MID Server to retrieve the temporary security credentials associated with an IAM role.

## Before you begin

Role required: discovery\_admin or sn\_cmp.cloud\_admin \(for Cloud Provisioning and Governance\)

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **MID Servers**.

2.  Select a MID Server installed on an Amazon EC2 instance within the relevant AWS service account.

3.  Open the **Configuration Parameters** related list.

4.  Click **New**.

5.  In the configuration parameter form, select **mid.aws.instance\_profile\_name** in the **Parameter name** field.

6.  Enter the name of the IAM role attached to the EC2 Instance in the **Value** field.

    **Note:** AWS Cloud Discovery for "mid.aws.instance\_profile\_name" accepts both "role name" and "full ARN" as valid parameter values. For example, both of the following values are acceptable:

    -   arn:partition:service:region:account-id:resource-type/resource-id
    -   resource-id
    The MID Server uses the same IAM role that is set up for the corresponding AWS service account. For more information, see [Configure access using temporary credentials based on trusted AWS accounts with AWS credentials](configure-iam-role-aws-account.md).

    For operational information about creating AWS roles, refer to the Amazon documentation on [Creating a role to delegate permissions to an IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html).

7.  Click **Submit**.

    The new parameter is listed in the MID Server record.

    ![MID Server configuration parameter for IAM roles](../image/mid_config_param_iam.png)


**Parent Topic:**[Set up AWS service accounts](../concept/setup-aws-service-accounts.md)

