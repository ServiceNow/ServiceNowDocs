---
title: AWS VPN Gateway pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS virtual private gateways on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-vpn-gateway-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS VPN Gateway, AWS virtual private gateway, AWS discovery, AWS patterns, VPN Gateway pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS VPN Gateway pattern-based discovery

Discovery and Service Mapping Patterns finds AWS virtual private gateways on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - VPN Gateway \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name or ID, if no name tag is specified for the VPN gateway.|
|Object ID \[object\_id\]|The ID of the virtual private gateway.|
|Connection Type \[connection\_type\]|The type of VPN connection the virtual private gateway supports.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name or ID, if no name tag is specified for the VPN gateway endpoint.|
|Object ID \[object\_id\]|The ID of the virtual private gateway.|
|Region \[region\]|The AWS region of the virtual private gateway endpoint.|

## CI relationships and references

The Amazon AWS - VPN Gateway \(LP\) pattern creates the following relationships and references to support AWS VPN Gateway discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Implement End Point To::Implement End Point From|Virtual Private Gateway Endpoint \[cmdb\_ci\_endpoint\_vpg\]|
|Cloud Network \[cmdb\_ci\_network\]|Use End Point To::Use End Point From|Virtual Private Gateway Endpoint \[cmdb\_ci\_endpoint\_vpg\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|

## AWS Tag discovery

The Amazon AWS - VPN Gateway \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

