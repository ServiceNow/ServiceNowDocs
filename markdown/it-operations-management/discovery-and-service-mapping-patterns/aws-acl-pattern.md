---
title: AWS Network ACL pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Network access control lists \(ACLs\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery-and-service-mapping-patterns/aws-acl-pattern.html
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-03"
reading_time_minutes: 1
keywords: [AWS Network ACL, AWS ACL discovery, AWS patterns, Network ACL pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Network ACL pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Network access control lists \(ACLs\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [Amazon AWS Cloud components discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - ACL \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the network ACL.|
|Object ID \[object\_id\]|Unique identifier, allocated by AWS for this resource.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the endpoint.|
|Object ID \[object\_id\]|Unique identifier, allocated by AWS for this resource.|

## CI relationships

The Amazon AWS - ACL \(LP\) pattern creates the following relationships and references to support AWS Network ACL discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Network ACL \[cmdb\_ci\_network\_acl\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Network ACL \[cmdb\_ci\_network\_acl\]|
|Network ACL \[cmdb\_ci\_network\_acl\]|Implement End Point To::Implement End Point From|ACL Endpoint \[cmdb\_ci\_endpoint\_acl\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Use End Point To::Use End Point From|ACL Endpoint \[cmdb\_ci\_endpoint\_acl\]|

**Parent Topic:**[Available discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

