---
title: Azure hardware type pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure hardware type configurations on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-31"
reading_time_minutes: 2
keywords: [Azure - Hardware Type \(LP\), Azure - Cloud Hardware Type \(LP\), Azure VM size, Azure hardware configuration, Azure discovery, Azure patterns]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure hardware type pattern-based discovery

Discovery and Service Mapping Patterns finds Azure hardware type configurations on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the Azure - Hardware Type \(LP\) pattern to discover available Azure hardware type configurations \(VM sizes\) from your Azure account.

When using the Hardware Type \[cmdb\_ci\_compute\_template\] table to store the hardware types, you may notice an unusually large number of records. To avoid this issue, you can store the discovered hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. When enabled, Discovery launches the Azure - Cloud Hardware Type \(LP\) pattern to populate the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. For more information, see [Enable the Cloud Hardware Type class extension](../../discovery/task/enable-hardware-type-class-extension.md).

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure hardware type patterns.

<table id="table_hardware_type_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name of the hardware type configuration.For example: **Standard\_A1\_v2** or **Standard\_D2s\_v3**.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The name of the hardware type configuration.For example: **Standard\_A1\_v2** or **Standard\_D2s\_v3**.

</td></tr><tr><td>

Cores \[cores\]

</td><td>

The number of CPU cores available for this hardware type configuration.

</td></tr><tr><td>

Memory MB \[memory\_mb\]

</td><td>

The amount of memory available for this hardware type configuration, in megabytes \(MB\).

</td></tr><tr><td>

vCPUs \[vcpus\]

</td><td>

The number of Virtual Central Processing Units \(vCPUs\) available for this hardware type configuration.

</td></tr><tr><td>

Local Storage GB \[local\_storage\_gb\]

</td><td>

The size of the temporary disk \(resource disk\) available for this hardware type configuration, in gigabytes \(GB\).

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **AZURE**. This field is only populated in Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

</td></tr></tbody>
</table>## CI relationships

The Azure hardware type patterns create these relationships to support Azure hardware type discovery.

|CI|Relationship|CI|
|---|------------|---|
|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md)

