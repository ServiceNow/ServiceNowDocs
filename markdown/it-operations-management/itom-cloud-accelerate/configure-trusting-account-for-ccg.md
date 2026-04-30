---
title: Configure the trusting account for Cloud Configuration Governance and Cloud Action Library
description: Configure the trusting account whose resources need to be accessed, to rely on the trusted account using the Identity and Access Management \(IAM\) role.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Set up Cloud Configuration Governance for AWS, Exploring Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Configure the trusting account for Cloud Configuration Governance and Cloud Action Library

Configure the trusting account whose resources need to be accessed, to rely on the trusted account using the Identity and Access Management \(IAM\) role.

## Before you begin

-   Familiarize yourself with the Amazon documentation on [Creating a role to delegate permissions to an IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html).
-   Decide which Amazon Web Services \(AWS\) account is going to be the trusted account. You use the trusted account to configure temporary credentials for Cloud Configuration Governance using IAM roles. The trusted account that you use to access other accounts using IAM roles is referred to as an accessor account.
-   Set up the trusted and the trusting account as described in [Set up Cloud Configuration Governance for AWS](set-up-ccg-for-aws.md).

Role required: sn\_itom\_ccg.scheduling\_admin

## Procedure

1.  Create an IAM role for the trusting account and configure the trust relationship between the user assuming this role and the trusted \(accessor\) account.

    1.  Log in to the trusting account on the AWS Management Console.

    2.  Create and configure the IAM role specifying the trusted \(accessor\) account ID in the **Account ID** field.

        For information on creating AWS roles, see the [Amazon documentation](https://docs.aws.amazon.com/).

    3.  On the Summary page for the IAM role, select the **Trust Relationships** tab.

    4.  Select **Edit trust relationship**.

        The Edit Trust Relationship page opens showing the policy document.

    5.  Set the **AWS** parameter to the full user ARN of the trusted \(accessor\) account.

        ![Editing trust relationship for the trusting account.](../../it-operations-management/image/aws-edit-trust-relat-trusting-iam.png)

    6.  Verify that the **Action** value is set to **sts:AssumeRole**.

    7.  Select **Update Trust Policy**.

2.  Configure the trusted service account for the trusting account in the ServiceNow AI Platform.

    1.  Navigate to **** **Cloud Provisioning and Governance** &gt; **Service Accounts**.

    2.  Open the trusting account.

    3.  On the Cloud Service Account form, enter the name of the trusted account in the **Accessor account** field.

    4.  Select **Update**.

3.  Create an assume role configuration for the trusting account.

    For more information, see [Create an assume role configuration](../../it-operations-management/task/create-assume-role-config.md).


**Parent Topic:**[Set up Cloud Configuration Governance for AWS](set-up-ccg-for-aws.md)

