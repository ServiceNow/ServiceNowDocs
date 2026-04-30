---
title: Create a workload provider type
description: Create a workload provider type for each new configuration management provider. This information appears in the order catalog form as management attributes that your users can select when provisioning a virtual resource through a configuration management provider.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a workload provider type

Create a workload provider type for each new configuration management provider. This information appears in the order catalog form as management attributes that your users can select when provisioning a virtual resource through a configuration management provider.

## Before you begin

Role required: cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Config Management**.

2.  Click **Workload Config Provider Types**, and then click **New**.

3.  Fill in the form fields \(as shown in the table\).

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the workload provider type.|
    |Product Type|A cloud product type from the list.|
    |Config CI|Select the configuration table created for the provider that displays the discovered resources from the list.|
    |Credential Resolver|Select a credential resolver from the list.|
    |Server Type|Select the type of server for the provider like Opensourced, Enterprise, etc.|
    |Version|Enter the version of the provider.|
    |Credential Type|Select the table where the credentials are stored for this provider.|

    ![Ansible tower](../image/workload-config-provider-example.png "Example Ansible Tower workload provider type")

4.  Add properties for the workload type in the **Workload Provider Properties** section.

    In addition to the existing properties, you can add more properties. Workload provider properties are displayed in the order catalog form \(in the Cloud User Portal\) as management attributes.

    For example, for an Ansible provider type, **Inventory**, and **Hostgroup** are mandatory. The values for these properties come from Resource Pools.

5.  Click **Submit**.


