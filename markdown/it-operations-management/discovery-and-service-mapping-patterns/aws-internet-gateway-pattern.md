---
title: AWS Internet Gateway pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Internet Gateways in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-internet-gateway-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 2
keywords: [Amazon AWS Internet Gateway, AWS Internet Gateway discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Internet Gateway pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Internet Gateways in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Internet Gateway \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or ID if no Name is specified for the internet gateway.|
|Object ID \[object\_id\]|ID of the internet gateway.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name or ID if no Name is specified for the internet gateway.|
|Object ID \[object\_id\]|ID of the internet gateway.|

## CI relationships

The Amazon AWS - Internet Gateway \(LP\) pattern creates the following relationships and references to support AWS Internet Gateway discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Internet Gateway \[cmdb\_ci\_internet\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Internet Gateway \[cmdb\_ci\_internet\_gateway\]|Implement End Point To::Implement End Point From|Internet Gateway Endpoint \[cmdb\_ci\_endpoint\_intgateway\]|
|Cloud Network \[cmdb\_ci\_network\]|Use End Point To::Use End Point From|Internet Gateway Endpoint \[cmdb\_ci\_endpoint\_intgateway\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Internet Gateway \[cmdb\_ci\_internet\_gateway\]|

## AWS Tag discovery

The Amazon AWS - Internet Gateway \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Internet Gateway \[cmdb\_ci\_internet\_gateway\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

