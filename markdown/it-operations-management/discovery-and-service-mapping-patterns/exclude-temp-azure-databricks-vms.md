---
title: Exclude temporary Azure Databricks virtual machines
description: Reduce short-lived configuration item \(CI\) records by excluding temporary Azure Databricks virtual machines \(VMs\).
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Azure virtual machine, Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Exclude temporary Azure Databricks virtual machines

Reduce short-lived configuration item \(CI\) records by excluding temporary Azure Databricks virtual machines \(VMs\).

## Before you begin

Verify that you have at least version 1.30.2 of Discovery and Service Mapping Patterns.

Role required: admin

## About this task

By default, Discovery includes temporary Azure Databricks VMs in discovery results. The **glide.discovery.cloud.filterout\_databrick\_vms** system property controls whether these VMs are excluded from the CMDB. The default value is **false**. When set to true, Discovery excludes Azure Databricks VMs during pattern-based discovery, reducing the number of short-lived CI records in your CMDB.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `glide.discovery.cloud.filterout_databrick_vms`.

3.  Select the **glide.discovery.cloud.filterout\_databrick\_vms** system property.

4.  In the **Value** field, enter **true**.

5.  Select **Update**.


**Parent Topic:**[Azure virtual machine pattern-based discovery](../reference/azure-vm-pattern.md)

**Related topics**  


[Azure virtual machine pattern-based discovery](../reference/azure-vm-pattern.md)

[Microsoft Azure Cloud discovery using patterns](../reference/azure-cloud-discovery-patterns.md)

