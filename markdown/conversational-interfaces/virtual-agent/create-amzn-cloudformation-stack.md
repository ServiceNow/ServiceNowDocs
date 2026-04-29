---
title: Create an Amazon CloudFormation Stack
description: Create an AWS CloudFormation stack to provision all the infrastructure resources required to enable the Conversational IVR feature. You will be populating a template provided by ServiceNow that will then generate the required configuration.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure AWS account, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create an Amazon CloudFormation Stack

Create an AWS CloudFormation stack to provision all the infrastructure resources required to enable the Conversational IVR feature. You will be populating a template provided by ServiceNow that will then generate the required configuration.

## Before you begin

Role required: admin

Ensure that you downloaded the Cloud Formation Template \(CFT\) YAML file from this [Knowledge Article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1430643) before creating an Amazon CloudFormation Stack and also make sure that you select the same region as that of the S3 bucket region.

For more information about creating an Amazon CloudFormation stack, refer to [Amazon CloudFormation documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html).

## Procedure

1.  Log in to the Amazon Web Services Console.

2.  Navigate to **CloudFormation** &gt; **Stacks**.

3.  Click the **Create stack** drop-down and select **With new resources \(standard\)**.

4.  On the Create stack form, under Prepare template section, select **Template is Ready**.

5.  In the Template resource section, select **Upload a template file** to the choose your downloaded CFT template and click **Next**.

    You will be directed to the Specify stack details page.

6.  On the Specify stack details page, provide a **Stack name** \(for example: sn-ci-cc-amazon-connect-setup-stack\) and specify the following details in the Parameters section:

<table id="table_jg5_cnh_kvb"><thead><tr><th>

Parameters

</th><th>

Description

</th><th>

Example Value

</th></tr></thead><tbody><tr><td colspan="3">

AWS Configuration

</td></tr><tr><td>

**S3 Bucket Name**

</td><td>

The name of the S3 Bucket that you created during the IVR setup process. S3 bucket must contain the required files to be uploaded. Populate this parameter with that bucket name.

</td><td>

sn-ci-cc-amazon-connect-setup

</td></tr><tr><td colspan="3">

ServiceNow Instance Configuration

</td></tr><tr><td>

ServiceNow Instance

</td><td>

The URL of the ServiceNow instance being used in this configuration. Be sure to include `https://`.

</td><td>

https://\[instance-name\].service-now.com

</td></tr><tr><td>

Username

</td><td>

Name of the ServiceNow user to be used for establishing a basic authentication configuration in your ServiceNow instance.The user with this username must have the 'sn\_va\_as\_service.contact\_center\_api' role.

</td><td>

n/a

</td></tr><tr><td>

Password

</td><td>

ServiceNow user's password to establish a basic authentication configuration in your ServiceNow instance.

</td><td>

n/a

</td></tr><tr><td>

Token Type

</td><td>

The type of token used in this connection. If you do not know the token type, then use Static.

</td><td>

Static/Hash

</td></tr><tr><td>

Token Value

</td><td>

The secure token value for the connection between Amazon Connect and ServiceNow.**Note:** Ensure that the token you provide does not contain any non-alphanumeric values and ensure that you save the token value for later use.

</td><td>

rLRU5tyNHVj39MdA

</td></tr><tr><td colspan="3">

Amazon Connect Instance Configuration - \(Ignore if there is an existing amazon connect instance\)

</td></tr><tr><td>

Amazon connect instance alias

</td><td>

Name for the Amazon Connect instance that will be created.

</td><td>

n/a

</td></tr><tr><td>

Prompt audio S3 file key

</td><td>

Provide the name of the Prompt file that you have uploaded in [Create an Amazon S3 bucket](create-amazon-s3-bucket.md).The Prompt file is an audio file containing the ringtone when customer connects to an agent.

</td><td>

n/a

</td></tr><tr><td colspan="3">

Amazon Connect Instance Admin Configuration \(Optional\)

</td></tr><tr><td>

Username

</td><td>

Provide an Amazon Connect username to create the administrator for the newly created Amazon Connect instance.

</td><td>

n/a

</td></tr><tr><td>

Email

</td><td>

Email of the administrator for the Amazon Connect instance.

</td><td>

n/a

</td></tr><tr><td>

First Name

</td><td>

First name of the user who is the administrator of the Amazon Connect instance.

</td><td>

n/a

</td></tr><tr><td>

Last Name

</td><td>

Last name of the user who is the administrator of the Amazon Connect instance.

</td><td>

n/a

</td></tr><tr><td>

Password

</td><td>

Password to log into the Amazon Connect instance as an administrator.

</td><td>

n/a

</td></tr></tbody>
</table>7.  Click **Next**.

8.  Review the parameters that you provided for your Stack, select the **I acknowledge that AWS CloudFormation might create IAM resources with custom names.** checkbox, and **Submit**.

    The Stack creates the required resources needed for the Amazon Connect IVR setup.

9.  Review the progress of the CloudFormation Stack to ensure that the process completes with a CREATE\_COMPLETE status.

    Once the Cloud Formation Stack is created, you will see the Amazon Connect instance.


## What to do next

[Claim a phone number](claim-phone-nmbr-ivr.md).

**Parent Topic:**[Configuring your AWS account for use with Conversational IVR](../concept/configure-aws-account.md)

