---
title: Configure access using temporary credentials based on trusted AWS accounts with AWS credentials
description: Configure the trusting account whose resources need to be accessed, to rely on the trusted account using the Identity and Access Management \(IAM\) role.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setting up AWS service accounts, Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Configure access using temporary credentials based on trusted AWS accounts with AWS credentials

Configure the trusting account whose resources need to be accessed, to rely on the trusted account using the Identity and Access Management \(IAM\) role.

## Before you begin

-   Familiarize yourself with the Amazon documentation on [Creating a role to delegate permissions to an IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html).
-   Decide which AWS account is going to be the trusted account. You use the trusted account to configure temporary credentials for Cloud Discovery using IAM roles. The trusted account that you use to access other accounts using IAM roles is referred to as an accessor account.
-   If you're setting up a trust chain where a member account trusts a management account, and the management account trusts an accessor account, verify that you've configured the member account to trust the management account. For more information, see [Configure access using temporary credentials for trusting AWS member accounts in management-accessor trust chain](configure-iam-role-aws-member.md).
-   Confirm that Discovery Admin Workspace is using at least version 1.10.0. The **Discovery** &gt; **Cloud Service Accounts** navigation module isn't available with earlier versions. To access **Cloud Service Accounts** with an earlier version, enter in the navigation filter: `cmdb_ci_cloud_service_account.list`.

Role required:

-   For Cloud Discovery: discovery\_admin
-   For Cloud Provisioning and Governance: admin or sn\_cmp.cloud\_admin

## About this task

During this configuration, you create an IAM role for the trusting account, and then configure the trusted service account for the trusting account at ServiceNow AI Platform. Finally, you associate the IAM role you created for the trusting account with the trusting account itself.

![Set up the IAM role of the trusting AWS account to trust the user of the trusted AWS account for access](../image/aws-any-account-trusted-with-credentials.png "Setting up any AWS account to rely on a trusted account with AWS credentials")

## Procedure

1.  Create an IAM role for the trusting account and configure the trust relationship between the user assuming this role and the trusted \(accessor\) account.

    1.  Log in to the trusting account on the AWS Management Console.

    2.  Create and configure the IAM role specifying the trusted \(accessor\) account ID in the **Account ID** field.

        For information on creating AWS roles, see the [Amazon documentation](https://docs.aws.amazon.com/).

    3.  On the Summary page for the IAM role, select the **Trust Relationships** tab.

    4.  Select **Edit trust relationship**.

        The Edit Trust Relationship page opens showing the policy document.

    5.  Set the **AWS** parameter to the full user ARN of the trusted \(accessor\) account.

        ![Editing trust relationship for the trusting account.](../image/aws-edit-trust-relat-trusting-iam.png)

    6.  Verify that the **Action** value is set to **sts:AssumeRole**.

    7.  Select **Update Trust Policy**.

2.  On the ServiceNow AI Platform, configure the trusted service account.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**.

    2.  Selelct **New**.

    3.  On the form, fill in the fields.

        For a description of the field values, see [Create AWS service accounts](create-aws-service-accounts.md).

    4.  Select **Submit**.

3.  On the ServiceNow AI Platform, configure the trusting service account.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**.

    2.  Select **New**.

    3.  In the **Accessor account** field, enter the name of the trusted account.

    4.  On the form, fill in the remaining fields.

        For a description of the field values, see [Create AWS service accounts](create-aws-service-accounts.md).

    5.  Select **Submit**.

4.  On the ServiceNow AI Platform, assign the AWS IAM role to the trusting account, using the relevant form, based on the relationship to the trusted account.

<table id="choicetable_g1z_335_zfc"><thead><tr><th align="left" id="d603511e433">

Trusted account type

</th><th align="left" id="d603511e436">

Steps

</th></tr></thead><tbody><tr><td id="d603511e442">

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


</td></tr><tr><td id="d603511e559">

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

