---
title: AWS VPN Connections pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Virtual Private Network \(VPN\) connections on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/aws-vpn-connections-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS VPN Connections, AWS VPN, AWS discovery, AWS patterns, VPN connection pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS VPN Connections pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Virtual Private Network \(VPN\) connections on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - VPN Connections \(LP\) pattern.

**Note:** This pattern is not supported for CN regions.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name or ID, if no name tag is specified for the VPN connection.|
|Object ID \[object\_id\]|The ID of the VPN connection.|
|State \[state\]|The current state of the VPN connection. The following values are valid: pending, available, deleting, or deleted.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The ID of the customer gateway.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The ID of the virtual private gateway.|

## CI relationships and references

The Amazon AWS - VPN Connections \(LP\) pattern creates the following relationships and references to support AWS VPN Connections discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|VPN Connection \[cmdb\_ci\_vpn\_connection\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Customer Gateway \[cmdb\_ci\_customer\_gateway\]|Contains::Contained by|VPN Connection \[cmdb\_ci\_vpn\_connection\]|
|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Contains::Contained by|VPN Connection \[cmdb\_ci\_vpn\_connection\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|VPN Connection \[cmdb\_ci\_vpn\_connection\]|

## AWS Tag discovery

The Amazon AWS - VPN Connections \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the VPN Connection \[cmdb\_ci\_vpn\_connection\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

