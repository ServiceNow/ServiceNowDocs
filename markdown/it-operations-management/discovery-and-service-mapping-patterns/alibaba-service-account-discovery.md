---
title: Alibaba Cloud service account pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Alibaba - Service Account Validation pattern to discover service accounts during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Alibaba, Service Account Validation]
breadcrumb: [Alibaba Cloud discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Alibaba Cloud service account pattern-based discovery

Discovery and Service Mapping Patterns uses the Alibaba - Service Account Validation pattern to discover service accounts during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Alibaba Cloud discovery prerequisites section in [Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Alibaba - Service Account Validation pattern.

<table id="table_w42_kwl_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Alibaba Cloud Resource Name \(ARN\) of the current requester.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The ID of the Alibaba Cloud account to which the current requester belongs.

</td></tr><tr><td>

Datacenter Type \[datacenter\_type\]

</td><td>

Type of the datacenter where the account is hosted: Alibaba Datacenter \[cmdb\_ci\_alibaba\_datacenter\].

</td></tr><tr><td>

Account Id \[account\_id\]

</td><td>

The ID of the Alibaba Cloud account to which the current requester belongs.

</td></tr><tr><td>

Discovery credentials \[discovery\_credentials\]

</td><td>

Alibaba Cloud API credentials.

</td></tr><tr><td>

Datacenter URL \[datacenter\_url\]

</td><td>

Datacenter URL.Example URLs:

-   For GovCloud: **https://ecs.aliyun-inc.com**
-   For commercial cloud: **htpps://ecs.aliyuncs.com**

</td></tr></tbody>
</table>## CI relationships

Discovery creates this reference to support the Alibaba Cloud service account discovery.

|CI|Relationship|CI|
|---|------------|---|
|Key Value \[cmdb\_key\_value\]|References|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Tag discovery

The Alibaba - Service Account Validation pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag key.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table.|

**Parent Topic:**[Alibaba Cloud discovery using patterns](../concept/alibaba-cloud-discovery-pattern.md)

