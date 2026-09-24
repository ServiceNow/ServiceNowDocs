---
title: AWS NAT Gateway pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Network Address Translation \(NAT\) Gateways in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-nat-gateway-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 2
keywords: [Amazon AWS NAT Gateway, AWS NAT Gateway discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS NAT Gateway pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Network Address Translation \(NAT\) Gateways in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - NAT Gateway \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the NAT gateway.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the NAT endpoint.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|

## CI relationships and references

The Amazon AWS - NAT Gateway \(LP\) pattern creates the following relationships and references to support AWS NAT Gateway discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|Implement End Point To::Implement End Point From|NAT Endpoint \[cmdb\_ci\_endpoint\_nat\]|
|Cloud Network \[cmdb\_ci\_network\]|Use End Point To::Use End Point From|NAT Endpoint \[cmdb\_ci\_endpoint\_nat\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|

## AWS Tag discovery

The Amazon AWS - NAT Gateway \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the NAT Gateway \[cmdb\_ci\_nat\_gateway\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

