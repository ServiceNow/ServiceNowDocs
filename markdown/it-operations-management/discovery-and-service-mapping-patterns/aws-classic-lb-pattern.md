---
title: AWS Classic Load Balancer pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Classic Load Balancers on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-classic-lb-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 3
keywords: [Amazon AWS Classic Load Balancer, AWS Classic LB discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Classic Load Balancer pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Classic Load Balancers on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Classic LB \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer.|
|Fully Qualified Domain Name \[fqdn\]|The DNS name of the load balancer.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|
|DNS Name \[dns\_name\]|The DNS name of the load balancer.|
|Canonical Hosted Zone Name \[canonical\_hosted\_zone\_name\]|The DNS name of the load balancer.|
|Canonical Hosted Zone ID \[canonical\_hosted\_zone\_id\]|The ID of the Amazon Route 53 hosted zone for the load balancer.|

|Field|Description|
|-----|-----------|
|Name \[name\]|IP address of the load balancer.|
|Object ID \[object\_id\]|IP address of the load balancer.|
|IP Address \[ip\_address\]|IP address of the load balancer.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Domain Name System \(DNS\).|
|IP Address \[ip\_address\]|IP address of the DNS.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer pool.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer pool member \(known in AWS as a target\).|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer service.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|
|Port \[port\]|The port on which the load balancer is listening.|
|Service port \[service\_port\]|The port on which the load balancer is listening.|
|Server protocol \[service\_protocol\]|The protocol to use for routing traffic to instances: HTTP, HTTPS, TCP, or SSL.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

## CI relationships and references

The Amazon AWS - Classic LB \(LP\) pattern creates the following relationships and references to support AWS Classic Load Balancer discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|DNS Name \[cmdb\_ci\_dns\_name\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

## AWS Tag discovery

The Amazon AWS - Classic LB \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

