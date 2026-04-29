---
title: Create a relationship between a VMware network and subnet
description: If you discover VMware networks and subnets, you must manually create a relationship between the two.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [IPAM integration, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a relationship between a VMware network and subnet

If you discover VMware networks and subnets, you must manually create a relationship between the two.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## About this task

If no relationship exists and a user must select a virtual network and subnet in the Cloud User Portal, the user can encounter an error.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Service Accounts**.

2.  Open the datacenter that contains the VMware cloud network.

    **Note:** VMware cloud networks are saved in the VMware vCenter Network \[cmdb\_ci\_vcenter\_network\] table. AWS and Azure cloud networks are saved in the Cloud Networks `[cmdb_ci_network]` table.

3.  Under **Related items**, click the plus icon to add a new relationship.

4.  Make sure the **Use suggested relationships** check box is selected, and then select the **Contains \(Parent\)** relationship.

5.  Under **Filter**, create the filter necessary to find the subnet.

6.  Under **Configuration Items**, select the check box next to the subnet.

7.  In the **Relationships** section, click the plus icon.

    The relationship is added to the list.

8.  Click **Save and Exit**.


