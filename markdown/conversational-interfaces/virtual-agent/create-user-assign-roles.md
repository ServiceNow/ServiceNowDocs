---
title: Grant access to an IAM \(Identity and Access Management\) role
description: Grant a ServiceNow user the required permissions to complete the Conversational Integration with Amazon Connect on the AWS Console.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure AWS account, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Grant access to an IAM \(Identity and Access Management\) role

Grant a ServiceNow user the required permissions to complete the Conversational Integration with Amazon Connect on the AWS Console.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your AWS \(Amazon Web Services\) account and search for **IAM**.

2.  Navigate to **Users**.

3.  Click **Add users**, provide the **User name**, and click **Next**.

4.  On the Set permissions page, under Permissions options, select **Attach policies directly** and select the following permissions:

    -   AWSLambdaExecute
    -   AmazonConnect\_FullAccess
    -   AmazonS3FullAccess
    **Note:** You can search and select the attachments at the **Permissions policies** search bar.![Attach policies to the IAM user for configuring IVR.](../images/ivr-attach-policies-iam-user.png)

5.  After selecting the required roles, click **Next**.

6.  Click **Create user**.


**Parent Topic:**[Configuring your AWS account for use with Conversational IVR](../concept/configure-aws-account.md)

