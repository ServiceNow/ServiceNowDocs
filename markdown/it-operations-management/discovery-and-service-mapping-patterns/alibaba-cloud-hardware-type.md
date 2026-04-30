---
title: Alibaba Cloud cloud hardware type pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Alibaba - Cloud Hardware Type \(LP\) pattern to discover cloud hardware types during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-10-22"
reading_time_minutes: 1
keywords: [Alibaba, Cloud Hardware Type, Alibaba Cloud discovery, Alibaba Cloud patterns, Alibaba Cloud Cloud Hardware Type discovery]
breadcrumb: [Alibaba Cloud discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud cloud hardware type pattern-based discovery

Discovery and Service Mapping Patterns uses the Alibaba - Cloud Hardware Type \(LP\) pattern to discover cloud hardware types during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Alibaba Cloud discovery prerequisites section in [Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Alibaba - Cloud Hardware Type \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|ID of the instance type.|
|vCPUs \[vcpus\]|Number of virtual central processing units \(vCPUs\).|
|Memory MB \[memory\_mb\]|Memory size in megabytes \(MB\).|
|Local Storage GB \[local\_storage\_gb\]|Capacity of each local disk in gigabytes \(GB\).|
|Name \[name\]|Image name.|
|Provider \[provider\]|Image cloud provider: Alibaba.|
|Cores \[cores\]|Number of CPU cores.|

## CI relationships

Discovery creates these relationships to support the cloud hardware type discovery.

|CI|Relationship|CI|
|---|------------|---|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\]|

**Parent Topic:**[Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md)

