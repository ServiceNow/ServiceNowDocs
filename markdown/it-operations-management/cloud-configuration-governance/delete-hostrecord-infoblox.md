---
title: Delete a host record in Infoblox
description: When a virtual machine is de-provisioned, delete the host record from Infoblox. Deleting the host record enables that IP address to be available and be reused for other virtual machines.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IPAM integration, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Delete a host record in Infoblox

When a virtual machine is de-provisioned, delete the host record from Infoblox. Deleting the host record enables that IP address to be available and be reused for other virtual machines.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Click **New**.

3.  Fill out the fields on the Policy form \(see table\).

    |Field|Value|
    |-----|-----|
    |**Policy Name**|Enter a descriptive name.|
    |**Policy Trigger**|Select **on Resource operation**.|
    |**Resource Block**|Select **ResourceBlock Virtual Server**.|
    |**Operation**|Select **Virtual Server interface Deprovision**.|
    |**Moment**|Select **Post Operation**.|

4.  Click **Submit** to publish the policy.

5.  Create a policy rule for the policy and click **Update**.

6.  In the **Policy Rules Action** related list, click **New** to create a policy action.

7.  Select **IP Address Management** in the **Create Policy Rule Action** dialog box.

    Enter a name in the **Action Name** field, select **Infoblox** in the **Provider Type** list, and select **Release IP address** in the **IPAM Method Name** list.

8.  Click **Submit**.

9.  In the **Policy Rule Action Attributes** section, enter the domain name of your company network in the **DNSSuffix** field.

    As an example, `corp.servicenow.com`. Values for all the other properties are already populated.

10. Click **Update** and republish the policy.


