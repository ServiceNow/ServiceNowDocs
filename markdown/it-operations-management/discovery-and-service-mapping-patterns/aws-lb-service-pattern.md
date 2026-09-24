---
title: AWS LB Service pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS load balancer \(LB\) listeners in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-lb-service-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 1
keywords: [Amazon AWS LB Service, AWS load balancer service discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS LB Service pattern-based discovery

Discovery and Service Mapping Patterns finds AWS load balancer \(LB\) listeners in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - LB Service \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer service.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|
|Port \[port\]|The port on which the load balancer is listening.|
|Service port \[service\_port\]|The port on which the load balancer is listening.|
|Server protocol \[service\_protocol\]|The protocol to use for routing traffic to instances: HTTP, HTTPS, TCP, or SSL.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

## CI relationships

The Amazon AWS - LB Service \(LP\) pattern creates the following relationships to support AWS LB Service discovery.

|CI|Relationship|CI|
|---|------------|---|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

