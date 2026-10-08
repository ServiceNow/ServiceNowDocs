---
title: AWS subnet pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS subnets on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-subnet-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS Subnet, AWS subnet, AWS discovery, AWS patterns, Subnet pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS subnet pattern-based discovery

Discovery and Service Mapping Patterns finds AWS subnets on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Subnet \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name or ID, if no name is specified for the subnet.|
|Object ID \[object\_id\]|The ID of the subnet.|
|CIDR \[cidr\]|The IPv4 CIDR block assigned to the subnet. If an IPv6 CIDR block is also assigned, it is appended to the IPv4 value.|
|Available IP Count \[available\_ip\_count\]|The number of unused private IPv4 addresses in the subnet. The IPv4 addresses for any stopped instances are considered unavailable.|
|State \[state\]|The current state of the subnet. The following values are valid: pending or available.|
|Gateway \[gateway\]|ID of the internet gateway attached to the subnet, if applicable.|

## CI relationships and references

The Amazon AWS - Subnet \(LP\) pattern creates the following relationships and references to support AWS Subnet discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|

## AWS Tag discovery

The Amazon AWS - Subnet \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Subnet \[cmdb\_ci\_cloud\_subnet\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

