---
title: AWS Organizational Units pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Organizational Units in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-organizational-units-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS Organizational Units, AWS Organizations, AWS discovery, AWS patterns, Organizational Units pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Organizational Units pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Organizational Units in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Organizational Units \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The user-friendly name of the Organizational Unit \(OU\).|
|Object ID \[object\_id\]|The unique identifier \(ID\) associated with this OU. The ID is unique to the organization.|
|Organizational ID \[aws\_org\_id\]|The unique ID associated with this OU. The ID is unique to the organization.|
|Org Unit Parent ID \[org\_unit\_parent\_id\]|The ID of the root or the immediate parent OU.|
|Root ID \[root\_id\]|The unique ID of the root of the organization.|

## CI relationships and references

The Amazon AWS - Organizational Units \(LP\) pattern creates the following relationships and references to support AWS Organizational Units discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|
|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|Contains::Contained by|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|

## AWS Tag discovery

The Amazon AWS - Organizational Units \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

