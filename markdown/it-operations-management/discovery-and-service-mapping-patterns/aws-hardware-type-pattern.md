---
title: AWS hardware type pattern-based discovery
description: Discovery and Service Mapping Patterns finds Amazon EC2 instance types on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-30"
reading_time_minutes: 2
keywords: [Amazon AWS - Hardware Type, Amazon AWS - Cloud Hardware Type, AWS instance type, AWS EC2, AWS discovery, AWS patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS hardware type pattern-based discovery

Discovery and Service Mapping Patterns finds Amazon EC2 instance types on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the Amazon AWS - Hardware Type \(LP\) pattern to discover AWS EC2 instance types from your AWS account.

When using the Hardware Type \[cmdb\_ci\_compute\_template\] table to store the hardware types, you may notice an unusually large number of records. To avoid this issue, you can store the discovered hardware types in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. When enabled, Discovery launches the Amazon AWS - Cloud Hardware Type \(LP\) pattern to populate the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. For more information, see [Enable the Cloud Hardware Type class extension](../../discovery/task/enable-hardware-type-class-extension.md).

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the AWS hardware type patterns.

<table id="table_hardware_type_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the instance type.For example: t2.micro or m5.large

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Name of the instance type.For example: t2.micro or m5.large

</td></tr><tr><td>

Cores \[cores\]

</td><td>

The default number of cores for the instance type.

</td></tr><tr><td>

Memory MB \[memory\_mb\]

</td><td>

The size of the memory for the instance type, in megabytes \(MB\).

</td></tr><tr><td>

vCPUs \[vcpus\]

</td><td>

The default number of Virtual Central Processing Units \(vCPUs\) for the instance type.

</td></tr><tr><td>

Local Storage GB \[local\_storage\_gb\]

</td><td>

The total size of the local instance storage for the instance type, in gigabytes \(GB\).

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **AWS**. This field is only populated in Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table.

</td></tr></tbody>
</table>## CI relationships

The AWS hardware type patterns create these relationships to support AWS hardware type discovery.

|CI|Relationship|CI|
|---|------------|---|
|Hardware Type \[cmdb\_ci\_compute\_template\] or Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

