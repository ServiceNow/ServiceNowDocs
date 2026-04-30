---
title: Alibaba Cloud availability zone pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Alibaba - Availability Zone \(LP\) pattern to discover availability zones during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-10-22"
reading_time_minutes: 1
keywords: [Alibaba, Alibaba Cloud, Alibaba Cloud discovery, Alibaba Cloud patterns, Alibaba Cloud availability zone pattern, Alibaba Cloud availability zone discovery]
breadcrumb: [Alibaba Cloud discovery, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud availability zone pattern-based discovery

Discovery and Service Mapping Patterns uses the Alibaba - Availability Zone \(LP\) pattern to discover availability zones during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Alibaba Cloud discovery prerequisites section in [Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Alibaba - Availability Zone \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Zone ID of the Alibaba Cloud availability zone.|
|Object ID \[object\_id\]|Zone ID of the Alibaba Cloud availability zone.|
|Install Status \[install\_status\]|Install status of the availability zone. Default value is Installed.|

## CI relationships

Discovery creates these relationships to support the availability zone discovery.

|CI|Relationship|CI|
|---|------------|---|
|Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

**Parent Topic:**[Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md)

