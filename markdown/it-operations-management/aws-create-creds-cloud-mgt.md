---
title: Configure access to the AWS accounts using permanent AWS credentials
description: To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery and Cloud Provisioning and Governance, you first create a user with programmatic access in the AWS Management Console. You then securely store the credentials in a service account at ServiceNow AI Platform.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Set up AWS service accounts, Setting up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Configure access to the AWS accounts using permanent AWS credentials

To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery and Cloud Provisioning and Governance, you first create a user with programmatic access in the AWS Management Console. You then securely store the credentials in a service account at ServiceNow AI Platform.

## Before you begin

Roles required:

-   AWS Management Console administrator
-   For Cloud Discovery: discovery\_admin
-   For Cloud Provisioning and Governance: admin or sn\_cmp.cloud\_admin

## About this task

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings.

## Procedure

1.  To create a user for Cloud Provisioning and Governance \(for programmatic access to your AWS resource and billing data\), perform the following steps.

    1.  On the AWS Management Console, navigate to **Identity and Access Managements \(IAM\)** &gt; **Access Management** &gt; **Users**.

    2.  On the IAM Resources portal, select **Users**.

    3.  Select **Add user**.

    4.  On the Details page, configure the user settings, and then select **Next**.

        |Field|Description|
        |-----|-----------|
        |User name|Name for the programmatic user. For example, `servicenowcloud`.|
        |Access type|Select **Programmatic access**.|

    5.  On the Permissions page, attach the user to a policy.

        Configure the following settings and then select **Next**.

<table id="table_k3c_n4v_ndb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set permissions for &lt;user name&gt;

</td><td>

Select **Attach existing policies directly**.

</td></tr><tr><td>

Attach one or more policies …

</td><td>

Select the appropriate policy. **Note:** The **AdministratorAccess** policy has the most powerful permission level, including permission to provision cloud resources. The policy enables the same access that would be granted to the instance if you were not using IAM and used your AWS account Access Key ID and Secret Access Key. You might instead prefer to create a policy or combine multiple policies to grant the appropriate permission level. See [Control AWS access and permissions using policies](aws-create-user-policy-cloud-mgt.md) for details.

</td></tr></tbody>
</table>    6.  On the Review page, verify your selections and then select **Create user**.

    7.  On the Security Credentials page, copy the secret access key and the access key ID.

        **Important:** Do not leave the page until you have completed both steps. The **Secret access key** value does not appear again. You need to paste the values that you generate in these steps into a Cloud Provisioning and Governance form.

        1.  Select **Show** to display the Secret access key. Copy the value.
        2.  Select **Download .csv** to save the CSV-format file that contains the user name, Access key ID, and the Secret access key value. You create the file as a backup in the case that you lose the values. Verify that the file was created and then store the file securely.
2.  On the ServiceNow AI Platform, configure AWS credentials.

    1.  In the ServiceNow instance, navigate to **Discovery** &gt; **Credentials**.

    2.  Select **New**, select **AWS Credentials**, enter a unique and meaningful **Name** \(for example, `Cloud Provisioning Account`\), and then fill in the form.

<table id="table_jsq_gxn_jw"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for the AWS credentials.

</td></tr><tr><td>

Active

</td><td>

Option to use the credential.

</td></tr><tr><td>

Access Key ID

</td><td>

The **Access key ID** that you generated on the AWS Management Console, such as: APIAIOSFODNN7EXAMPLE.

</td></tr><tr><td>

Secret access key

</td><td>

The **Secret access key** that you generated on the AWS Management Console, such as: wPalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY.

</td></tr></tbody>
</table>    3.  Select **Update** or **Submit**.


## What to do next

Create an AWS service account on the ServiceNow AI Platform. For more information, see [Create AWS service accounts](create-aws-service-accounts.md).

**Parent Topic:**[Set up AWS service accounts](../concept/setup-aws-service-accounts.md)

