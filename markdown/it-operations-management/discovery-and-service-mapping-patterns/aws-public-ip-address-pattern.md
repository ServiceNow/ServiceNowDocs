---
title: AWS Public IP Address pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS public IP addresses \(Elastic IPs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-public-ip-address-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 1
keywords: [Amazon AWS Public IP Address, AWS Elastic IP discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Public IP Address pattern-based discovery

Discovery and Service Mapping Patterns finds AWS public IP addresses \(Elastic IPs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Public IP Address \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or allocation ID if no Name is specified for the public IP address.|
|Object ID \[object\_id\]|The ID representing the allocation of the address for use with EC2-VPC.|
|Public IP Address \[public\_ip\]|The Elastic IP address.|

## CI relationships and references

The Amazon AWS - Public IP Address \(LP\) pattern creates the following relationships and references to support AWS Public IP Address discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|

## AWS Tag discovery

The Amazon AWS - Public IP Address \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

