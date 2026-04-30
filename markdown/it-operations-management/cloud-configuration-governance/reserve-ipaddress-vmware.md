---
title: Reserve IP addresses for VMware vSphere virtual machines in InfoBlox
description: Create a policy to reserve IP addresses for VMware vSphere virtual machines in Infoblox, at the time of provisioning the virtual machines.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IPAM integration, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Reserve IP addresses for VMware vSphere virtual machines in InfoBlox

Create a policy to reserve IP addresses for VMware vSphere virtual machines in Infoblox, at the time of provisioning the virtual machines.

## Before you begin

Role required: sn\_cmp.cloud\_admin.

## About this task

You can create a policy that is invoked when a VMware virtual machine is provisioned to get an IP address from Infoblox. Before the virtual machine is provisioned, the instance makes a call to Infoblox that creates a host record with the IP address.

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

5.  Specify a condition in the condition builder for locating the vSphere virtual machine.

6.  Select **Request from** &gt; **starts with** and enter `vSphere`.

7.  Click **Update**.

8.  In the **Policy Rules Action** related list, click **New** to create a policy action.

9.  Select **IP Address Management** in the **Create Policy Rule Action** dialog box.

10. Enter a name in the **Action Name** field, select **Infoblox** in the **Provider Type** list, and select **Reserve IP address** in the **IPAM Method Name** list.

11. Click **Submit**.

12. In the **Policy Rule Action Attributes** section, enter the domain name of your network in the **DNSSuffix** field.

    As an example,`corp.servicenow.com`. Values for all the other properties are already populated.

13. Click **Update** and republish the policy.


