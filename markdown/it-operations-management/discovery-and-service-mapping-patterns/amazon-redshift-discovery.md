---
title: Amazon Redshift discovery with Patterns
description: The ServiceNow Discovery application uses the Amazon AWS Redshift pattern to find Redshift data warehouse services available on Amazon Web Services \(AWS\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Amazon Redshift, AWS patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon Redshift discovery with Patterns

The ServiceNow® Discovery application uses the Amazon AWS Redshift pattern to find Redshift data warehouse services available on Amazon Web Services \(AWS\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Redshift runs as a cluster of compute nodes with an additional leader node. The leader node acts as an interface with client applications and coordinates communication between the compute nodes.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS Redshift pattern.

<table id="table_pw1_srb_b5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Redshift cluster.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier constructed from the Redshift namespace Amazon Resource Name \(ARN\) and the cluster name in the following format: **arn:aws:redshift:&lt;region&gt;:&lt;account-id&gt;:cluster:&lt;cluster-name&gt;**.

</td></tr><tr><td>

Start date \[start\_date\]

</td><td>

Timestamp when the Redshift cluster was created.

</td></tr><tr><td>

Cluster Availability Status \[cluster\_availability\_status\]

</td><td>

Current availability status of the Redshift cluster.For example: Available, Unavailable, or Maintenance.

</td></tr><tr><td>

VPC ID \[vpc\_id\]

</td><td>

ID of the virtual private cloud \(VPC\) in which the Redshift cluster is deployed.

</td></tr><tr><td>

Node Count \[node\_count\]

</td><td>

Total number of compute nodes in the Redshift cluster.

</td></tr><tr><td>

Node Type \[node\_type\]

</td><td>

Type of compute nodes used in the Redshift cluster.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Fully qualified domain name \(FQDN\) of the Redshift cluster endpoint.

</td></tr><tr><td>

TCP port\(s\) \[tcp\_port\]

</td><td>

TCP port used by the Redshift cluster for client connections.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address associated with the Redshift cluster endpoint.

</td></tr><tr><td>

Availability Zone \[availability\_zone\]

</td><td>

References the Availability Zone \[cmdb\_ci\_availability\_zone\] table.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the avaiability zone.|
|Object ID \[object\_id\]|Name of the avaiability zone.|

## CI relationships

Discovery creates these relationships to support the Amazon Redshift discovery.

|CI|Relationship|CI|
|---|------------|---|
|Amazon Redshift \[cmdb\_ci\_aws\_redshift\]|References|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Key Value \[cmdb\_key\_value\]|References|Amazon Redshift \[cmdb\_ci\_aws\_redshift\]|

## Tag discovery

The Amazon AWS Redshift pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Amazon Redshift \[cmdb\_ci\_aws\_redshift\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

