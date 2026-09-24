---
title: AWS Availability Zone pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Availability Zones in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-availability-zone-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 1
keywords: [Amazon AWS Availability Zone, AWS Availability Zone discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Availability Zone pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Availability Zones in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Availability Zone \(LP\) pattern.

<table id="table_mkf_2hc_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Availability Zone.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier, allocated by Amazon for this resource.

</td></tr><tr><td>

State \[state\]

</td><td>

The state of the Availability Zone. Possible values are: available, information, impaired, or unavailable.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - Availability Zone \(LP\) pattern creates the following relationships to support AWS Availability Zone discovery.

|CI|Relationship|CI|
|---|------------|---|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

