---
title: Register IP addresses for AWS and Azure virtual machines in Infoblox
description: Create a policy to register IP addresses for AWS and Azure virtual machines in Infoblox, once these virtual machines are provisioned.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IPAM integration, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Register IP addresses for AWS and Azure virtual machines in Infoblox

Create a policy to register IP addresses for AWS and Azure virtual machines in Infoblox, once these virtual machines are provisioned.

## Before you begin

Role required: sn\_cmp.cloud\_admin.

## About this task

When AWS and Azure virtual machines are provisioned, IP addresses are automatically allocated to them. You can create a policy and the policy is invoked, once these virtual machines are provisioned, to get their IP addresses and register these IP addresses in Infoblox.

**Note:** This functionality is not supported with our template-based cloud catalogs.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Click **New** and then fill in the form.

    |Field|Description|
    |-----|-----------|
    |Policy Name|Enter a descriptive name.|
    |Policy Trigger|Select **on Resource operation**.|
    |Resource Block|Select **ResourceBlock Virtual Server**.|
    |Operation|Select **Virtual Server interface provision**.|
    |Moment|Select **Pre Operation**.|

3.  Click **Submit** to publish the policy.

4.  Create a policy rule for the policy.

    Specify two conditions in the condition builder for locating the AWS and the Azure virtual machines. Select **Request form** &gt; **starts with** and enter `AWS`. Specify another condition for Azure.

5.  Click **Update**.

6.  In the **Policy Rules Action** related list, click **New** to create a policy action.

7.  Select **IP Address Management** in the **Create Policy Rule Action** dialog box.

    Enter a name in the **Action Name** field, select **Infoblox** in the **Provider Type** list, and select **Register IP address** in the **IPAM Method Name** list.

8.  Click **Submit**.

9.  In the **Policy Rule Action Attributes** section, enter the domain name of your company's network in the **DNSSuffix** field.

    As an example,`corp.servicenow.com`. Values for all the other properties are already populated.

10. Click **Update** and republish the policy.


