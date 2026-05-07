---
title: Set up suspension of an AWS account using service control policy
description: Set up a restriction on cloud account creation. For example, when the account owner isn’t in the organization or if there are budget constraints. Using Cloud Account Management, admin adds the account number to the AWS organization's service control policy, promoting existing accounts to continue to function normally while blocking new account creation.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Configuring Service Control Policy in AWS, Setting up AWS cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up suspension of an AWS account using service control policy

Set up a restriction on cloud account creation. For example, when the account owner isn’t in the organization or if there are budget constraints. Using Cloud Account Management, admin adds the account number to the AWS organization's service control policy, promoting existing accounts to continue to function normally while blocking new account creation.

## Before you begin

Verify you have saved the CloudFormation template. For more details, see [Configuring Service Control Policy in AWS](about-service-control-policy.md).

Role required: AWS admin

## Procedure

1.  Log in to the AWS Management console.

2.  Enter `CloudFormation` in the search bar and then select it.

3.  On the CloudFormation console, select **Create Stack**.

4.  On the **Create Stack** page, select **Choose an existing template** &gt; **Upload a template file** &gt; **Choose file** to choose a template file from your local computer.

5.  Select **Next** to continue and to validate the template.

6.  On the **Specify stack details** page, enter a `CloudFormation stack name` in the **Stack name** field.

    The stack name is an identifier that helps you find a particular stack from a list of stacks. A stack name can contain only alphanumeric characters \(case-sensitive\) and hyphens. It must start with an alphabetic character and can't be longer than 128 characters.

7.  Select **Next** and then select **Submit**.


## Result

Once the CloudFormation Template \(CFT\) creates the policy, an Amazon Resource Name \(ARN\) is assigned. An ARN typically follows the format:

```
arn:aws:organizations::1234567890:policy/o-99t3h155el/service_control_policy/p-328wg3yb
```

To view the ARN, go to **AWS Organization** &gt; **Policies** &gt; **Service control policies** &gt; **CAM\_SCP\_SupsendAccount\_policy**.

The key element that you must provide to the ServiceNow AI Platform admin is the policy element, which in this example is: p-328wg3yb.

## What to do next

[Provisioning modes for Cloud Account Management in Cloud Workspace](../concept/supported-provision-modes.md)

