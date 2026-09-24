---
title: AWS IP Address pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS IP addresses associated with network interfaces in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-ip-address-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 1
keywords: [Amazon AWS IP Address, AWS IP Address discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS IP Address pattern-based discovery

Discovery and Service Mapping Patterns finds AWS IP addresses associated with network interfaces in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - IP Address \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or ID if no Name is specified for the network interface.|
|IP Address \[ip\_address\]|If available, the address of the Elastic IP address bound to the network interface. If not available, the private IP.|
|Object ID \[object\_id\]|The ID of the network interface.|
|Public DNS \[public\_dns\]|The public DNS name, if available.|
|Private IP Address \[private\_ip\]|The IPv4 address of the network interface within the subnet.|
|Instance ID \[instance\_id\]|The ID of the instance.|

## CI relationships

The Amazon AWS - IP Address \(LP\) pattern creates the following relationships to support AWS IP Address discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\]|Contains::Contained by|IP Address \[cmdb\_ci\_cloud\_ip\_address\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

