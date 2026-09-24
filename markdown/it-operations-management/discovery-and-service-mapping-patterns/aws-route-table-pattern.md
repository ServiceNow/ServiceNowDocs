---
title: AWS Route Table pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS route tables in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-route-table-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS Route Table, AWS route table, AWS discovery, AWS patterns, Route Table pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Route Table pattern-based discovery

Discovery and Service Mapping Patterns finds AWS route tables in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Route Table \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name tag of the route table, or the route table ID if no Name tag is specified.|
|Object ID \[object\_id\]|The ID of the route table.|
|State \[state\]|If the route table is discoverable, the value is set to **available**.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name tag of the route table, or the route table ID if no Name tag is specified.|
|Object ID \[object\_id\]|The ID of the route table.|

## CI relationships and references

The Amazon AWS - Route Table \(LP\) pattern creates the following relationships and references to support AWS Route Table discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Route Table \[cmdb\_ci\_route\_table\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Use End Point To::Use End Point From|Route Table Endpoint \[cmdb\_ci\_endpoint\_route\_table\]|
|Route Table \[cmdb\_ci\_route\_table\]|Implement End Point To::Implement End Point From|Route Table Endpoint \[cmdb\_ci\_endpoint\_route\_table\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Route Table \[cmdb\_ci\_route\_table\]|

## AWS Tag discovery

The Amazon AWS - Route Table \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Route Table \[cmdb\_ci\_route\_table\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

