---
title: Server CI population during cloud discovery
description: Cloud discovery can populate Server CIs without running IP-based discovery, reducing discovery time in large environments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/server-ci-cloud-discovery.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-05-14"
reading_time_minutes: 4
keywords: [cloud discovery, Server CI, Windows Server, Linux Server, pattern extension]
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Server CI population during cloud discovery

Cloud discovery can populate Server CIs without running IP-based discovery, reducing discovery time in large environments.

## Server CI cloud discovery overview

By default, cloud discovery creates Virtual Machine \(VM\) Instance CIs only. To populate Server CIs, organizations run IP-based discovery, which triggers a separate schedule that discovers servers alongside applications and other data. In large environments, IP-based discovery schedules can take a significant amount of time. Some organizations require only server records from their cloud environment, without discovering application data.

Starting with Discovery and Service Mapping Patterns version 1.31.0, cloud discovery can create Windows Server CIs, Linux Server CIs, or both alongside Virtual Machine Instance CIs, without running IP-based discovery. The **sn\_itom\_pattern.cloud\_discovery\_populate\_server\_ci** system property controls whether Server CIs are created. By default, the property is set to none and Server CIs aren't created. For more information, see [Configure Server CI creation during cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-server-ci-cloud-disc.md).

The following patterns support Server CI population during cloud discovery:

-   Azure – Virtual Machine \(LP\)
-   Azure VM Instance – Uniform Scale Set

**Note:** Use either Server CI population during cloud discovery or IP-based discovery for the same VMs, but not both. Running both may result in conflicting attribute values.

## Data collected by Discovery during horizontal discovery

Discovery populates the following data when running the Azure – Create Server CI pattern extension. Virtual Desktop Infrastructure \(VDI\) instances can't be distinguished from other VMs and are registered as Windows Server or Linux Server CIs.

<table id="table_server_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Hostname of the server. The name is sourced from one of the following options:-   If the VM is running: the VM computer name
-   If the VM is stopped: the OS profile computer name
-   If the VM is stopped and the Server CI already exists in the CMDB: the existing name is retained

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier for the server, matching the Azure VM object ID.

</td></tr><tr><td>

CPU Core Count \[cpu\_core\_count\]

</td><td>

Number of CPU cores, derived from the VM size.

</td></tr><tr><td>

CPU Count \[cpu\_count\]

</td><td>

Number of CPUs. Default value is 1.

</td></tr><tr><td>

Disk Space \(GB\) \[disk\_space\]

</td><td>

Total storage capacity of all disks attached to the VM, in gigabytes \(GB\).

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the server. Default value is Installed.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the server, sourced from the primary VM network interface.

</td></tr><tr><td>

Is Virtual \[virtual\]

</td><td>

Indicates the server is a virtual machine. Default value is true.

</td></tr><tr><td>

Operating System \[os\]

</td><td>

Operating system name.

</td></tr><tr><td>

Operational Status \[operational\_status\]

</td><td>

Operational status of the server. Default value is Operational.

</td></tr><tr><td>

OS Version \[os\_version\]

</td><td>

Operating system version, if available.

</td></tr><tr><td>

RAM \(MB\) \[ram\]

</td><td>

Memory capacity in megabytes \(MB\), derived from the VM size.

</td></tr><tr><td>

Serial Number \[serial\_number\]

</td><td>

Unique identifier for the server, sourced from the Azure VM ID.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Serial Number \[serial\_number\]|Unique identifier, sourced from the Azure VM ID.|
|Serial Number Type \[serial\_number\_type\]|Type of serial number. Default value is uuid.|
|Valid \[valid\]|Indicates the serial number is valid. Default value is true.|
|Configuration Item \[cmdb\_ci\]|References the Windows Server \[cmdb\_ci\_win\_server\] or Linux Server \[cmdb\_ci\_linux\_server\] table.|

## CI relationships

The Azure – Create Server CI pattern extension creates the following relationships and references to support Server CI discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Windows Server \[cmdb\_ci\_win\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Linux Server \[cmdb\_ci\_linux\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Serial Number \[cmdb\_serial\_number\]|Configuration Item \[cmdb\_ci\]|Windows Server \[cmdb\_ci\_win\_server\]|
|Serial Number \[cmdb\_serial\_number\]|Configuration Item \[cmdb\_ci\]|Linux Server \[cmdb\_ci\_linux\_server\]|

-   **[Configure Server CI creation during cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-server-ci-cloud-disc.md)**  
Create Server CIs during cloud discovery without running IP-based discovery, reducing discovery time in large environments.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md)

**Previous topic:**[Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md)

**Next topic:**[Configure Server CI creation during cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-server-ci-cloud-disc.md)

**Related topics**  


[Azure virtual machine pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/azure-vm-pattern.md)

[Azure Virtual Machine Scale Sets \(VMSS\) Instance discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/AzureVMScaleSetInstance.md)

