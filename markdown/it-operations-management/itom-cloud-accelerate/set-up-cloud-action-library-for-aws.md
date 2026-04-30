---
title: Set up Cloud Action Library for AWS
description: Set up access to the Amazon Web Services \(AWS\) cloud accounts in Cloud Action Library to enable interaction between the application and the cloud.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Exploring Cloud Action Library, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Cloud Action Library for AWS

Set up access to the Amazon Web Services \(AWS\) cloud accounts in Cloud Action Library to enable interaction between the application and the cloud.

## Before you begin

Role required: admin

## About this task

For the purposes of configuring access for AWS accounts, the following terms are used:

-   **Trusting accounts**

    The trusting accounts don't have permanent AWS credentials. You configure the trust relationship for IAM roles in these accounts to rely on other accounts for access.

-   **Trusted accounts**

    The trusted accounts are used by the trusting accounts for access. The ServiceNow UI refers to the trusted accounts as accessor accounts.


Use any one of the following methods to configure access to the AWS accounts:

-   Configure the permanent credentials in the ServiceNow AI Platform to connect with the standalone AWS accounts \(discreet accounts\). The Cloud Service Account \[cmdb\_ci\_cloud\_service-account\] table contains information on the service account type, such as management or member account and access credentials.
-   Configure the member accounts to rely on the management account for access. In this case, configure the permanent credentials of the management account in the ServiceNow AI Platform.
-   Configure the accounts to rely on a trusted account for access \(lateral access within the same AWS organization or across different AWS organizations\). In this case, configure the permanent credentials of the trusted account in the ServiceNow AI Platform.

**Note:** Cloud Action Library doesn't use a MID Server-based assume role setup to access the trusting accounts.

## Procedure

1.  Create credentials for the AWS service accounts.

    1.  Navigate to **Connection &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**, and then select **AWS Credentials**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique and descriptive name for the AWS credentials.|
        |Active|Option to use the credential.|
        |Access Key ID|The access key ID that you generated on the AWS management console.|
        |Secret Access Key|The secret access key that you generated on the AWS management console.|

    4.  Select **Save**.

2.  Select the **sn\_itom\_cal.Aws\_Creds\_Alias** credential alias or create a credential alias.

    1.  Unlock the credential alias.

    2.  Search for a credential alias.

    3.  Select **New**.

    4.  On the form, fill in the fields.

<table id="table_nhl_r2v_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the alias.

</td></tr><tr><td>

Type

</td><td>

Credential alias type.Select **Credential** from the Type drop-down list.

</td></tr></tbody>
</table>    5.  Select **Submit**.

3.  Set the **Authentication Algorithm** field to **AWS Authenticator**.

4.  Select **Submit**.

5.  Set up an AWS service account.

    1.  Navigate to **Cloud Provisioning and Governance** &gt; **Service accounts**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_azj_5fv_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the service account.

</td></tr><tr><td>

Account ID

</td><td>

12-digit user account number. Expand the list under the account name on the AWS Management Console to view the number.**Important:** In the **Account ID** field, remove the hyphen characters \(-\) from the number.

</td></tr><tr><td>

Discovery credentials

</td><td>

The credentials needed for ServiceNow applications to access the cloud account. You can configure the discovery credentials at a later stage, while configuring access to the AWS accounts.-   If you are setting up an independent service account or a management account, select its AWS credential.
-   To use other AWS accounts to access this account, leave the field empty.

For example, you don't have to specify the AWS credentials for accounts assuming Identity and Access Management \(IAM\) roles or member accounts using their management account for access.

</td></tr><tr><td>

Datacenter URL

</td><td>

URL of the datacenter.Leave this field empty.

</td></tr><tr><td>

Datacenter type

</td><td>

Type of the datacenter where the account is hosted.Select **AWS Datacenter**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Auto-generated value: Status and timestamp of the last execution of Discovery on the datacenter.

</td></tr><tr><td>

Parent account

</td><td>

Name of the management account that represents the AWS organization to which this member account belongs.This field appears when you select AWS Datacenter. If the account doesn't belong to any AWS organization, leave this field empty.

</td></tr><tr><td>

Is master account

</td><td>

Management account flag.This check box appears when you select AWS Datacenter from the Datacenter Type drop-down. Select the check box to associate the AWS service account with the management account. Select this check box only for accounts that you have previously configured as management accounts with some member accounts belonging to them. For more information on AWS Organization, see [AWS documentation](https://aws.amazon.com/documentation-overview/).

</td></tr><tr><td>

Accessor account

</td><td>

Name of the trusted account.Configure this field only for accounts that don't use permanent AWS credentials and rely on IAM roles for access.

</td></tr></tbody>
</table>    4.  Select **Submit**.

6.  To use a management account to scan the member accounts of the AWS organization, create an assume role configuration for the management account.

    1.  If you don't want to use the OrganizationAccountAccessRole to access the member account, Configure trusting account for Cloud Action Library.

        For more information, see [Configure the trusting account for Cloud Configuration Governance and Cloud Action Library](configure-trusting-account-for-ccg.md).

    2.  Repeat step [6.a](set-up-cloud-action-library-for-aws.md#create-trusting-acc-for-management-acc) for each member account that needs to be scanned through the management account without using the OrganizationAccountAccessRole.

    3.  If you want to use the OrganizationAccountAccessRole to access the member account, create an assume role configuration for the management account.

        For more information, see [Create an assume role configuration](../../it-operations-management/task/create-assume-role-config.md).

7.  To use a trusted account to scan the trusting account, configure trusting account for Cloud Action Library.

    The trusted account and trusting account can be in different AWS organizations or they can be in the same AWS organization.

    1.  Configure trusting account for Cloud Configuration Governance.

        For more information, see [Configure the trusting account for Cloud Configuration Governance and Cloud Action Library](configure-trusting-account-for-ccg.md).

    2.  Repeat step [7.a](set-up-cloud-action-library-for-aws.md#cuoss-assume-use-case-substep) for each trusting account that needs to be scanned through the trusted account.


**Parent Topic:**[Exploring Cloud Action Library](../concept/exploring-cloud-actions-library.md)

