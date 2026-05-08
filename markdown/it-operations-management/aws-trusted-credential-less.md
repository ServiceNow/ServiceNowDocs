---
title: Configure access using temporary credentials based on trusted AWS accounts without AWS credentials
description: Set up a trusted credential-less account that other AWS accounts can rely on for access.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Setting up AWS service accounts, Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Configure access using temporary credentials based on trusted AWS accounts without AWS credentials

Set up a trusted credential-less account that other AWS accounts can rely on for access.

## Before you begin

-   Familiarize yourself with the Amazon documentation on [Creating a role to delegate permissions to an IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html).
-   Decide which AWS account is going to be the trusted account. You use the trusted account to configure temporary credentials for Cloud Discovery using IAM roles. The trusted account that you use to access other accounts using IAM roles is referred to as an accessor account.
-   If you're setting up a trust chain where a member account trusts a management account, and the management account trusts an accessor account, verify that you've configured the member account to trust the management account. For more information, see [Configure access using temporary credentials for trusting AWS member accounts in management-accessor trust chain](configure-iam-role-aws-member.md).
-   Confirm that Discovery Admin Workspace is using at least version 1.10.0. The **Discovery** &gt; **Cloud Service Accounts** navigation module isn't available with earlier versions. To access **Cloud Service Accounts** with an earlier version, enter in the navigation filter: `cmdb_ci_cloud_service_account.list`.

Role required:

-   For Cloud Discovery: discovery\_admin
-   For Cloud Provisioning and Governance: admin or sn\_cmp.cloud\_admin

## About this task

To use an account without AWS credentials, you must first configure that account with an IAM role and permissions to access the trusting service account. Then, you set up the IAM role of the trusting account to grant access to the IAM role of the trusted account.

![Set up the IAM role of the trusting AWS account to trust the IAM role of the trusted AWS account for access](../image/aws-any-account-trusted-without-credentials.png "Setting up any AWS account to rely on a trusted account without AWS credentials")

## Procedure

1.  Configure an IAM role for the trusting account.

    1.  Log into the trusting account on the AWS Management Console.

    2.  Create an IAM role for this account.

        Use the account ID of the trusted account while creating this IAM role. For operational information about working with AWS roles, refer to the Amazon documentation.

    3.  [Create a ReadOnlyAccess policy](aws-create-user-policy-cloud-mgt.md) and attach it to the newly created IAM role.

2.  Configure the IAM role for the trusted account.

    1.  Log into the AWS Management Console using the credentials of the account that you want to set up as a trusted account.

    2.  Create an IAM role by choosing the **AWS service** option.

        ![Select the AWS service option for creating an IAM role of the trusted accout](../image/aws-role-aws-service-tile.png)

    3.  Create a read-only access policy for the trusted account IAM role.

        For more information, see [Control AWS access and permissions using policies](aws-create-user-policy-cloud-mgt.md).

    4.  Create an additional policy to grant this IAM role access to resources in trusting accounts:

        -   Set the **Action** parameter to `sts:AssumeRole`
        -   Set the **Resource** parameter to the ARN of the trusting account role that you created in [1.b](aws-trusted-credential-less.md#create-IAM-role-trusting-account).
        ![Configure the policy between the role in the trusted account and the role in the trusting account.](../image/aws-edit-policy-trusted-credential-less.png)

    5.  Attach the newly created role to the relevant Amazon EC2 instance.

        By default, when you attach an IAM role to an EC2 instance, it creates a trust relationship between this role and the EC2 instance.

        ![Verifying the trust relationship between the IAM role and the EC2 instance.](../image/aws-edit-trust-relat-ec2-instance.png)

3.  Configure the trusting service account to grant access to the IAM role belonging to the trusted account.

    1.  Log into the trusting account on the AWS Management Console.

    2.  Navigate to the IAM role you created for this account as described in [1.b](aws-trusted-credential-less.md#create-IAM-role-trusting-account).

    3.  Edit the Trust Relationship for this IAM role as follows:

        -   Set the **Action** parameter to `sts:AssumeRole`.
        -   Set the **AWS** parameter to the ARN of the trusted account role that you created in [2.b](aws-trusted-credential-less.md#create-role-trusted-account).
        ![Configure the trust relationship for the trusting account](../image/aws-edit-trust-relat-trusting-credential-less.png)

4.  Configure the MID Server for AWS IAM roles.

    For more information, see [Configure the MID Server for AWS IAM roles](config-mid-iam-roles.md).

5.  On the ServiceNow AI Platform, configure the trusted service account.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**.

    2.  Selelct **New**.

    3.  On the form, fill in the fields.

        For a description of the field values, see [Create AWS service accounts](create-aws-service-accounts.md).

    4.  Select **Submit**.

6.  On the ServiceNow AI Platform, configure the trusting service account.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**.

    2.  Select **New**.

    3.  In the **Accessor account** field, enter the name of the trusted account.

    4.  On the form, fill in the remaining fields.

        For a description of the field values, see [Create AWS service accounts](create-aws-service-accounts.md).

    5.  Select **Submit**.

7.  On the ServiceNow AI Platform, assign the AWS IAM role to the trusting account, using the relevant form, based on the relationship to the trusted account.

<table id="choicetable_g1z_335_zfc"><thead><tr><th align="left" id="d128130e593">

Trusted account type

</th><th align="left" id="d128130e596">

Steps

</th></tr></thead><tbody><tr><td id="d128130e602">

**Management account**

</td><td>

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Organization Access Parameters** &gt; **AWS Org Assume Role Parameters**.
2.  Select **New**.
3.  On the form, configure only the following fields for the trusting member account:

<table id="aws-org-assume-member-trusts-management"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Access role name

</td><td>

Name of the IAM role created for the trusting account.-   If IAM roles are the same across all member accounts: Enter the full ARN using an asterisk \(\*\) as a wildcard for the account ID in the format: `arn:aws:iam::*:role/MemberRoleName`.

For example: `arn:aws:iam::*:role/SN_MEMBER_ACCOUNT_ROLE`.

-   If IAM roles are different across member accounts: Enter the full ARN of the specific IAM role for each member account in a separate entry.


</td></tr><tr><td>

Cloud service account

</td><td>

Name of the trusting account for which you are providing access using the IAM role.-   If IAM roles are the same across all member accounts: Enter the management account name.
-   If IAM roles are different across member accounts: Enter each member account in a separate entry.


</td></tr></tbody>
</table>4.  Select **Submit**.


</td></tr><tr><td id="d128130e719">

**Member or discrete account**

</td><td>

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Organization Access Parameters** &gt; **AWS Cross Assume Role Parameters**.
2.  Select **New**.
3.  On the form, configure only the following fields for the trusting account:

    |Field|Description|
    |-----|-----------|
    |Access role name|Name of the IAM role created for the trusting account.|
    |Cloud service account|Name of the trusting account for which you are providing access using the IAM role.|

4.  Select **Submit**.


</td></tr></tbody>
</table>
## What to do next

Verify that ServiceNow applications can access the trusting service account using the IAM role:

1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**.
2.  Select the trusting AWS service account.
3.  Under **Related Links**, select **Create Discovery Schedule**.
4.  In the Discovery Manager Cloud Discovery page, select **Test Account**.
    -   If the connection is successful, a message displays indicating the account validation is successful.
    -   If the connection isn't successful, an error message displays indicating the cause of failure.

**Parent Topic:**[Setting up AWS service accounts](../concept/setup-aws-service-accounts.md)

