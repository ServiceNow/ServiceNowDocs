---
title: Create AWS GovCloud credentials for Cloud Provisioning and Governance
description: Skip this procedure if your organization does not use AWS GovCloud \(US\). To securely access data on your provider account, the Discovery process must present appropriate credentials. An AWS GovCloud \(US\) region is an isolated AWS region that meets stringent US government security and compliance requirements to host sensitive workloads. Cloud Provisioning and Governance supports all AWS GovCloud \(US\) services.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create AWS GovCloud credentials for Cloud Provisioning and Governance

Skip this procedure if your organization does not use AWS GovCloud \(US\). To securely access data on your provider account, the Discovery process must present appropriate credentials. An AWS GovCloud \(US\) region is an isolated AWS region that meets stringent US government security and compliance requirements to host sensitive workloads. Cloud Provisioning and Governance supports all AWS GovCloud \(US\) services.

## Before you begin

**Note:**

-   ServiceNow® ITOM products are not officially certified or supported against Germany and China regions.
-   Skip this procedure if your organization does not use AWS GovCloud \(US\).

-   You will need the AWS GovCloud \(US\) access key ID and the secret access key that you generated on the AWS Management Console.

Role required: sn\_cmp.cloud\_admin

## About this task

Cloud Provisioning and Governance accesses GovCloud regions using a set of credentials for each region. To configure Cloud Provisioning and Governance to support a GovCloud region, you create one standard AWS account for each region \(required for billing\), obtain the credentials for the account, and then create a service account for the region. For more information on billing, see the "AWS GovCloud \(US\) Billing and Payment" page in the [AWS documentation](https://aws.amazon.com/documentation/).

## Procedure

1.  On the AWS Management Console, enter `IAM` in the **AWS services** search box to open the Identity and Access Managements \(IAM\) service.

2.  On the IAM Resources portal, click **Users**.

3.  Create the Discovery user that has programmatic access to your AWS GovCloud \(US\) resource and billing data.

4.  Select **Add user**.

    On the Details page, configure the user settings, and then select **Next**.

<table id="table_kjt_hp5_ndb"><tbody><tr><td>

User name

</td><td>

Name for the programmatic user, for example, `servicenowcloud`.

</td></tr><tr><td>

Access type

</td><td>

Select **Programmatic access**.

</td></tr></tbody>
</table>5.  On the Permissions page, attach the user to a policy by configuring the following settings and then click **Next**.

<table id="table_k3c_n4v_ndb"><tbody><tr><td>

Set permissions for &lt;username&gt;

</td><td>

Select **Attach existing policies directly**.

</td></tr><tr><td>

Attach one or more policies …

</td><td>

Select the appropriate policy. **Note:** The **AdministratorAccess** policy has the most powerful permission level, including permission to provision cloud resources. The policy enables the same access that would be granted to the instance if you were not using IAM and used your AWS account Access Key ID and Secret Access Key. You might instead prefer to create a policy or combine multiple policies to grant the appropriate permission level. See [Control AWS access and permissions using policies](../../it-operations-management/task/aws-create-user-policy-cloud-mgt.md) for details.

</td></tr></tbody>
</table>6.  On the Review page, verify your selections and then click **Create user**.

7.  On the Complete page, perform two steps:

    **Note:** Do not leave the page until you have completed both steps. The **Secret access key** value will not appear again. Paste the values that you generate in these steps into a Cloud Provisioning and Governance form.

    1.  Click **Show** to display the Secret access key. Copy the value.
    2.  Click **Download .csv** to save the CSV-format file that contains the user name, Access key ID, and the Secret access key value. You create the file as a backup in the case that you lose the values. Verify that the file was created and then store the file securely.
8.  On your instance, navigate to **Orchestration** &gt; **Credentials &amp; Connections** &gt; **Credentials**.

9.  Click **New**, select **AWS Credentials**, enter a unique and meaningful **Name** \(for example, `AWS GovCloud Creds O1`\), and then fill in the form.

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
</table>10. Click **Submit**.

    The instance records the credentials. Next, you [Create a service account for AWS GovCloud](aws-govcloud-srv-acct-cloud-mgt-1.md).


