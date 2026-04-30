---
title: Configure access using temporary credentials for trusting AWS member accounts in management-accessor trust chain
description: Configure access for AWS member accounts by using a trust chain from the accessor through the management account.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-09-03"
reading_time_minutes: 3
breadcrumb: [Set up AWS service accounts, Setting up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Configure access using temporary credentials for trusting AWS member accounts in management-accessor trust chain

Configure access for AWS member accounts by using a trust chain from the accessor through the management account.

## Before you begin

-   Familiarize yourself with the Amazon documentation on [Creating a role to delegate permissions to an IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html).
-   Ensure that you know which AWS member accounts are assigned to the same management account. You use the management account for configuring temporary credentials for cloud discovery using IAM roles.
-   Confirm that Discovery Admin Workspace is using at least version 1.10.0. The **Discovery** &gt; **Cloud Service Accounts** navigation module isn't available with earlier versions. To access **Cloud Service Accounts** with an earlier version, enter in the navigation filter: `cmdb_ci_cloud_service_account.list`.

Role required:

-   For Cloud Discovery: discovery\_admin
-   For Cloud Provisioning and Governance: admin or sn\_cmp.cloud\_admin

## About this task

You can configure access for AWS member accounts by using a trust chain from the accessor through the management account. The accessor account either has AWS credentials or uses a credential-free method.

![Set up the IAM role of the trusting member accounts to trust their management account, which in turn trusts an accessor account](../image/aws-member-account-trusted-with-credentials.png "Configuring member accounts to use their management account for access")

## Procedure

1.  Create an IAM role for the member account and configure the trust relationship between the user assuming this role and the trusted management account.

    1.  Log into the AWS Management Console using the credentials of the member account for which you are configuring access.

    2.  Create and configure the IAM role specifying the management account ID in the **Account ID** field.

        For operational information about creating AWS roles, refer to the Amazon documentation.

    3.  On the **Summary** page for the IAM role, click the **Trust Relationships** tab.

    4.  Click **Edit trust relationship**.

        The Edit Trust Relationship page opens showing the policy document.

    5.  Edit the trust relationship as follows:

        -   Set the **Action** parameter to `sts:AssumeRole`
        -   Set the `AWS` parameter to the full role ARN of the management account.
        ![Editing trust relationship for the trusting account.](../image/aws-edit-trust-relat-member-iam.png)

    6.  Click **Update Trust Policy**.

2.  On the ServiceNow AI Platform, configure the trusting member's service account.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**.

    2.  Select **New**.

    3.  In the **Parent account** field, enter the name of the management account.

    4.  On the form, fill in the remaining fields.

        For a description of the field values, see [Create AWS service accounts](create-aws-service-accounts.md).

    5.  Select **Submit**.

3.  On the ServiceNow AI Platform, assign the AWS IAM role to the member account.

    **Important:** Perform this step only if you created custom IAM roles. By default, the OrganizationAccountAccessRole role is assigned to the member’s trusting management account and you don't need to assign the OrganizationAccountAccessRole role to a service account.

    1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Organization Access Parameters** &gt; **AWS Org Assume Role Parameters**.

    2.  Select **New**.

    3.  On the form, configure only the following fields for the trusting member account:

<table id="id_m4q_pq2_ngc"><thead><tr><th>

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
</table>    4.  Select **Submit**.


## What to do next

Configure the trusting management account and the trusted accessor account.

-   For information on configuring accessor accounts with AWS credentials, see [Configure access using temporary credentials based on trusted AWS accounts with AWS credentials](configure-iam-role-aws-account.md).
-   For information on configuring accessor accounts without AWS credentials, see [Configure access using temporary credentials based on trusted AWS accounts without AWS credentials](aws-trusted-credential-less.md).

**Parent Topic:**[Set up AWS service accounts](../concept/setup-aws-service-accounts.md)

