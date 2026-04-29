---
title: Set up a cloud account and service account for AWS
description: A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up a cloud account and service account for AWS

A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter. A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

## Before you begin

Role required: none

-   Operations in the AWS Management Console require the administrator role.
-   Operations in Cloud Provisioning and Governance require the sn\_cmp.cloud\_admin role.

## About this task

When you finish the Day-1 setup process, your cloud account might look like this:

![Structure of a cloud account on Day 1](../image/cloud-acct-day-1.png "Structure of a cloud account on Day 1")

## Procedure

1.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Cloud Accounts**.

2.  Select or create the cloud account:

    -   Select an existing cloud account:
        1.  On the Cloud Account page, click **Configure**.
        2.  On the General Information page, click **Next** and then continue with the next step.
    -   Create a cloud account:
        1.  On the General Information page, click **New** and then enter a unique and meaningful **Name** and **Description** for the cloud account.
        2.  Select the provider.
        3.  Click **Next** and then continue with the next step.
3.  On the Datacenters page, create a service account: Click the **+** next to the **Service Account** field, and then fill in the form for the service account.

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

 ![Determine the IAM user account number to fill in the Account ID field](../image/aws-account-id.png "IAM user account number")

</td></tr><tr><td>

Discovery credentials

</td><td>

The credentials needed for ServiceNow applications to access this account. You may configure this field at a later stage, while configuring access to AWS accounts.

 -   If you [configured AWS credentials at ServiceNow AI Platform](../../it-operations-management/task/aws-create-creds-cloud-mgt.md) , select the magnifying glass icon, and then select the name of the relevant AWS credential.
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

**Note:** You will need to setup the correct permission in AWS or the Organization role for a standard credential. For more information, see [Control AWS access and permissions using policies](../../it-operations-management/task/aws-create-user-policy-cloud-mgt.md).

</td></tr><tr><td>

Accessor account

</td><td>

Name of the trusted account. Configure this field only for accounts that don't use permanent AWS credentials and rely on IAM roles for access.

</td></tr></tbody>
</table>4.  Click **Submit** to create the service account.

5.  Click **Discover Datacenters**.

6.  When the datacenters appear, select one or more datacenters to include in the cloud account and then click **Save**.

    **Note:**

    -   Select only those LDCs/Regions where your infrastructure resources are present. If you don't have any resources under these new data centers, exclude them while you run the full discovery.
    -   To discover resources in regions/ LDCs such as, North America \(US East, US West and Canada Central\), South America, Europe, Africa, Middle East and Asia Pacific, raise an access request to the required endpoints with GCP Support.
    The Cloud Account dashboard appears. The datacenters that you selected appear on the **Datacenters** tab.

7.  Click a datacenter.

    The following lists appear:

    -   **Resources**: Cloud resources for the current datacenter. Run Discovery to populate the CMDB for the datacenter and populate the tab. See [Discover all datacenters in a service account on-demand](disco-datacntrs-in-srv-acct-1.md).
    -   **Capacity Limits**: Limits on virtual CPUs, virtual networks, storage volume size, and other services. See [Set capacity limits on user requests for resources](set-capacity-limits-cloud-mgt-1.md).
    -   **Discovery Log**: The process creates a log record for each action associated with a discovery status.

## What to do next

-   Configure additional permissions to provision Amazon AWS Cloud resources using Cloud Provisioning and Governance.
-   After you complete all procedures in this initial "Day 1" setup, you can create additional cloud accounts and service accounts to organize and compartmentalize your cloud infrastructure.

**Related topics**  


[Set up an additional cloud account](add-cloud-account-cloud-mgt.md)

[Add an AWS service account to the cloud account](aws-add-service-account-cloud-mgt.md)

