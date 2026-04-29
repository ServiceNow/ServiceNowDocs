---
title: Create a workload provider type
description: Create a workload provider type for each new configuration management provider. This information appears in the order catalog form as management attributes that your users can select when provisioning a virtual resource through a configuration management provider.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a workload provider type

Create a workload provider type for each new configuration management provider. This information appears in the order catalog form as management attributes that your users can select when provisioning a virtual resource through a configuration management provider.

## Before you begin

Role required: cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Config Management**.

2.  Select **Workload Config Provider Types**, and then select **New**.

3.  Fill in the form fields \(as shown in the table\).

<table id="table_pbd_2hp_l2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the workload provider type.

</td></tr><tr><td>

Product Type

</td><td>

A cloud product type from the list.

</td></tr><tr><td>

Config CI

</td><td>

Configuration table created for the provider that displays the discovered resources from the list.

</td></tr><tr><td>

Credential Resolver

</td><td>

A Credential Resolver translates a unique identifier into the actual user credentials.

</td></tr><tr><td>

Server Type

</td><td>

Type of server for the provider like Opensourced, Enterprise.

</td></tr><tr><td>

Version

</td><td>

Enter the version of the provider.For any new config provider type, a **Version** field needs to be added to the corresponding Name **\[config\_ci\]** table.

</td></tr><tr><td>

Credential Type

</td><td>

Types of credentials stored for this provider.

</td></tr></tbody>
</table>    ![Ansible tower](../image/workload-config-provider-example.png "Example Ansible Tower workload provider type")

4.  Add properties for the workload type in the **Workload Provider Properties** section.

    In addition to the existing properties, you can add more properties. Workload provider properties are displayed in the order catalog form \(in the Cloud User Portal\) as management attributes.

    For example, for an Ansible provider type, **Inventory**, and **Hostgroup** are required. The values for these properties come from Resource Pools.

5.  Select **Submit**.


