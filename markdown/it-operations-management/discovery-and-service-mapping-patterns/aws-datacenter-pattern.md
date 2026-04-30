---
title: AWS datacenter pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Regions for your AWS account on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-25"
reading_time_minutes: 1
keywords: [Amazon AWS datacenter discovery, AWS datacenters, AWS Regions, AWS Availability Zones, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS datacenter pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Regions for your AWS account on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS Datacenter discovery pattern.

<table id="table_mkf_2hc_dgc_csa"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Id \[account\_id\]

</td><td>

Unique identifier \(ID\) for the AWS service account.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique ID for the AWS service account.

</td></tr><tr><td>

Datacenter Type \[datacenter\_type\]

</td><td>

Type of datacenter. The value is set to **AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]**.

</td></tr></tbody>
</table><table id="table_aws_datacenter"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The AWS Region code.For example: us-east-1 or eu-central-1.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The AWS Region code.For example: us-east-1 or eu-central-1.

</td></tr><tr><td>

Region \[region\]

</td><td>

The AWS Region code.For example: us-east-1 or eu-central-1.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS Datacenter discovery pattern creates these relationships to support AWS datacenter discovery.

|CI|Relationship|CI|
|---|------------|---|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

