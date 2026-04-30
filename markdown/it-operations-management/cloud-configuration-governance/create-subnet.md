---
title: Create a cloud subnet
description: If you have subnets in your VMware vSphere account, create a cloud subnet record in the instance.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [IPAM integration, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a cloud subnet

If you have subnets in your VMware vSphere account, create a cloud subnet record in the instance.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Networks &amp; IPAM**.

2.  On the **IP Pools** tab, click **New** to create a new record.

3.  In the **Subnet** field, click the lookup icon.

    The Cloud Subnets list appears.

4.  Click **New**.

5.  Fill out the form fields \(see table\).

    |Field|Description|
    |-----|-----------|
    |Name|Provide a descriptive name.|
    |Status|Leave the status value as **Installed**.|
    |CIDR/Gateway/Subnet Mask|Enter the CIDR associated with the subnet, the IP address of the gateway, and the subnet mask. For VMware, the CIDR, Gateway, and Subnet Mask fields are mandatory.|
    |Primary and Secondary DNS|Enter the DNS values. For VMware, the Primary DNS field is mandatory.|

6.  Click **Submit**.


