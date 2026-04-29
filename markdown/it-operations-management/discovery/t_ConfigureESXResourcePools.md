---
title: Configure ESXi resource pools
description: The ESXi server has a default resource pool called Resources that defines normal resources for a virtual machine.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Configure ESXi, Configure resource pools, Configure ESXi servers]
breadcrumb: [Configure for VMware Discovery, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure ESXi resource pools

The ESXi server has a default resource pool called Resources that defines normal resources for a virtual machine.

## Before you begin

Role required: admin

## About this task

ESXi resource pools must be configured so Discovery can identify virtual machines and their relationships correctly. Resource levels are dynamically generated from shares of the total resources allocated to virtual machines on the ESXi server. For details about how these resources are calculated, review the VMware knowledge base [https://www.vmware.com/](https://www.vmware.com/). ServiceNow Discovery finds this default resource pool and adds a record to the ESXi Resource Pools module automatically.

If Discovery isn't running on the ServiceNow instance, create a record for the **Resources** pool. Verify that the **Owner** field is correct and leave the resource fields empty. If a provisioner selects the **Resources** pool when provisioning a virtual server, the ESXi server creates a virtual machine for use under a normal load.

## Procedure

1.  Navigate to **All** &gt; **VMware Cloud** &gt; **Configuration** &gt; **ESX Resource Pools**.

2.  Select **New** in the list.

3.  Create a record for each resource pool in the ESXi server, verifying that the **Name** and **Owner** fields are correct.

4.  Select the **CPU expandable** and **Memory expandable** check boxes.

    These features enable for expansion of the CPU and memory limits when needed, if those resources are available on the ESXi server. When granted, these extra resources can be revoked to provision other virtual machines. The additional fields on the form are for display purposes only.

5.  Select **Submit**.

    ![ESX Resource Pool form](../image/ESXResourcePool.png "ESX Resource Pool form")


