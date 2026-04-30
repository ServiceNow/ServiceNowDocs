---
title: Alibaba Cloud datacenter pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Alibaba - Datacenter \(LP\) pattern to discover datacenters during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-10-22"
reading_time_minutes: 1
keywords: [Datacenter, Alibaba Cloud, Alibaba Cloud datacenter discovery, Alibaba Cloud datacenter pattern, Alibaba Cloud patterns, Alibaba Cloud discovery]
breadcrumb: [Alibaba Cloud discovery, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud datacenter pattern-based discovery

Discovery and Service Mapping Patterns uses the Alibaba - Datacenter \(LP\) pattern to discover datacenters during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Alibaba Cloud discovery prerequisites section in [Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Alibaba - Datacenter \(LP\) pattern.

<table id="table_dqj_nwl_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

**LocalName** field value of the Alibaba Cloud region.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

**RegionId** field value of the Alibaba Cloud region.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the datacenter. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the datacenter. Default value is Operational.

</td></tr><tr><td>

Region \[region\]

</td><td>

**RegionId** field value of the Alibaba Cloud region.

</td></tr><tr><td>

Datacenter URL \[datacenter\_url\]

</td><td>

Datacenter URL.Example URLs:

-   For GovCloud: **https://ecs.aliyun-inc.com**
-   For commercial cloud: **htpps://ecs.aliyuncs.com**

</td></tr></tbody>
</table>## CI relationships

Discovery creates these relationships to support the Alibaba Cloud datacenter discovery.

|CI|Relationship|CI|
|---|------------|---|
|Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

**Parent Topic:**[Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md)

