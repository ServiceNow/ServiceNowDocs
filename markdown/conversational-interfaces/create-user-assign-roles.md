---
title: \(Legacy\) Grant access to an IAM \(Identity and Access Management\) role
description: Grant a ServiceNow user the required permissions to complete the Conversational Integration with Amazon Connect on the AWS Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/create-user-assign-roles.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure your AWS account, Configure, Conversational IVR with Amazon Connect, Integrate VA for NLU with voice channels, Virtual Agent channel integrations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Grant access to an IAM \(Identity and Access Management\) role

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
    **Note:** You can search and select the attachments at the **Permissions policies** search bar.\[Omitted image "ivr-attach-policies-iam-user.png"\] Alt text: Attach policies to the IAM user for configuring IVR.

5.  After selecting the required roles, click **Next**.

6.  Click **Create user**.


**Parent Topic:**[\(Legacy\) Configuring your AWS account for use with Conversational IVR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-aws-account.md)

