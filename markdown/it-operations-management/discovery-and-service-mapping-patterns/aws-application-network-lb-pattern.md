---
title: AWS Application and Network LB pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Application Load Balancers and Network Load Balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/aws-application-network-lb-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 2
keywords: [Amazon AWS Application Load Balancer, Amazon AWS Network Load Balancer, AWS load balancer discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Application and Network LB pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Application Load Balancers and Network Load Balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Application and Network LB \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer.|
|Fully Qualified Domain Name \[fqdn\]|IP address of the fully qualified domain name \(FQDN\) of the load balancer.|
|Object ID \[object\_id\]|The Amazon Resource Name \(ARN\) of the load balancer.|
|DNS Name \[dns\_name\]|The public Domain Name System \(DNS\) name of the load balancer.|
|Canonical Hosted Zone Name \[canonical\_hosted\_zone\_name\]|The name of the Amazon Route 53 hosted zone associated with the load balancer.|
|Canonical Hosted Zone ID \[canonical\_hosted\_zone\_id\]|The ID of the Amazon Route 53 hosted zone associated with the load balancer.|
|State \[state\]|The state of the load balancer.|
|Short Description \[short\_description\]|A concatenation of the series of attributes for the load balancer, including LB ARN, VPC ID, type, and zone.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the DNS.|
|Object ID \[object\_id\]|Name of the DNS.|
|IP Address \[ip\_address\]|IP address of the DNS.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

## CI relationships

The Amazon AWS - Application and Network LB \(LP\) pattern creates the following relationships and references to support AWS Application and Network LB discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|DNS Name \[cmdb\_ci\_dns\_name\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

## AWS Tag discovery

The Amazon AWS - Application and Network LB \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

