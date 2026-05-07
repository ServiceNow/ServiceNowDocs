---
title: Create an IP pool
description: Create an IP pool to associate a cloud subnet with an IPAM provider instance.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [IPAM integration, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create an IP pool

Create an IP pool to associate a cloud subnet with an IPAM provider instance.

## Before you begin

-   Role required: sn\_cmp.cloud\_admin
-   Create [Infoblox credentials](https://www.servicenow.com/docs/access?context=infoblox-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US) and [register an Infoblox server](create-infoblox.md).
-   Run Discovery on the cloud account to find subnets or [manually create cloud subnets](create-subnet.md).

**Note:** This functionality is not supported with our template-based cloud catalogs.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Networks &amp; IPAM**.

2.  On the **IP Pools** tab, click **New**, enter a unique and descriptive **Name**, and then fill in the form.

    ![Creating an IP pool](../image/create-ip-pool.png)

    |Field|Description|
    |-----|-----------|
    |IPAM Provider|Select an IPAM provider.|
    |Provider Instance|Select an instance for the provider.|
    |Provider Version|Enter a version for the provider.|
    |Subnet|Select a subnet. For AWS or Azure, select a discovered subnet that has been configured in AWS or Azure. For VMware, copy the CIDR range from the IPAM tool and paste the CIDR range in this field. See [Create a cloud subnet](create-subnet.md).|
    |Mode|Select a mode based on the provider that you are creating this IP pool for. The model varies based on the provider.|

3.  Click **Submit**.


## Result

The related subnet appears in the **Subnet** related list at the bottom of the form.

