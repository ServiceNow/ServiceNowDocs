---
title: AWS LB Pool pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS load balancer \(LB\) pools \(known in AWS as target groups\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-lb-pool-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 1
keywords: [Amazon AWS LB Pool, AWS load balancer pool discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS LB Pool pattern-based discovery

Discovery and Service Mapping Patterns finds AWS load balancer \(LB\) pools \(known in AWS as target groups\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - LB Pool \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer pool.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

## CI relationships

The Amazon AWS - LB Pool \(LP\) pattern creates the following relationships and references to support AWS LB Pool discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

