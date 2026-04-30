---
title: Configure ESXi resource pools
description: The ESXi server has a default resource pool called Resources that defines normal resources for a virtual machine.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 1
keywords: [Configure ESXi, Configure resource pools, Configure ESXi servers]
breadcrumb: [ESXi server, Discovery for VMware virtualization, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Configure ESXi resource pools

The ESXi server has a default resource pool called Resources that defines normal resources for a virtual machine.

## Before you begin

Role required: admin

## About this task

Resource levels are dynamically generated from shares of the total resources allocated to virtual machines on the ESXi server. For details about how these resources are calculated, review the VMware Knowledge Base [https://www.vmware.com/](https://www.vmware.com/). ServiceNow Discovery finds this default resource pool and adds a record to the ESXi Resource Pools module automatically. If Discovery is not running on the ServiceNow instance, create a record for the **Resources** pool. Ensure that the **Owner** field is correct and leave the resource fields blank. If a provisioner selects the **Resources** pool when provisioning a virtual server, the ESXi server will create a virtual machine for use under a normal load.

## Procedure

1.  Navigate to **All** &gt; **VMware Cloud** &gt; **Configuration** &gt; **ESX Resource Pools**.

2.  Click **New** in the list.

3.  Create a new record for each resource pool in the ESXi server, ensuring that the **Name** and **Owner** fields are correct.

4.  Select the **CPU expandable** and **Memory expandable** check boxes to allow for expansion of the CPU and memory limits when needed, if those resources are available on the ESXi server.

    When granted, these extra resources can be revoked if needed to provision other virtual machines. The additional fields on the form are for display purposes only.

5.  Click **Submit**.

    ![ESX Resource Pool form](../image/ESXResourcePool.png "ESX Resource Pool form")


**Parent Topic:**[ESXi server discovery](../reference/r_DiscoverESXServers.md)

