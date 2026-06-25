---
title: Configure Server CI creation during cloud discovery
description: Create Server CIs during cloud discovery without running IP-based discovery, reducing discovery time in large environments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/configure-server-ci-cloud-disc.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 1
keywords: [cloud discovery, Server CI, Windows Server, Linux Server, system property, pattern extension]
breadcrumb: [Server CI population during cloud discovery, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Configure Server CI creation during cloud discovery

Create Server CIs during cloud discovery without running IP-based discovery, reducing discovery time in large environments.

## Before you begin

Verify that you have at least version 1.31.0 of Discovery and Service Mapping Patterns.

Role required: admin

## About this task

The **sn\_itom\_pattern.cloud\_discovery\_populate\_server\_ci** property controls whether Server CIs are created during cloud discovery. By default, the property is set to none and Server CIs aren't created.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `sn_itom_pattern.cloud_discovery_populate_server_ci`.

3.  Select the **sn\_itom\_pattern.cloud\_discovery\_populate\_server\_ci** property.

4.  In the **Value** field, enter one of the following values.

    |Value|Description|
    |-----|-----------|
    |**none**|Server CIs aren't created. Default value.|
    |**windows\_only**|Windows Server CIs are created.|
    |**linux\_only**|Linux Server CIs are created.|
    |**all**|Windows Server CIs and Linux Server CIs are created for all VMs.|

5.  Select **Update**.


## What to do next

Run cloud discovery or wait for the next scheduled discovery run for the changes to apply.

**Parent Topic:**[Server CI population during cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/server-ci-cloud-discovery.md)

**Related topics**  


[Azure virtual machine pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-vm-pattern.md)

[Azure Virtual Machine Scale Sets \(VMSS\) Instance discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/AzureVMScaleSetInstance.md)

