---
title: Limit AWS discovery to datacenters with resources
description: Optimize AWS discovery by limiting it to datacenters with resources.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Limit AWS discovery to datacenters with resources

Optimize AWS discovery by limiting it to datacenters with resources.

## Before you begin

Verify that you have installed Discovery and Service Mapping Patterns, starting with version 1.29.0.

Role required: discovery\_admin

## About this task

Starting with version 1.29.0, Discovery and Service Mapping Patterns introduces a new AWS datacenter discovery model that focuses discovery on datacenters with resources and excludes datacenters that don't contain resource. To limit discovery to datacenters that contain resources, set the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** MID Server property to false. For more information, see [AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for the `mid.cloud.discovery.sonar.discover_all_aws_datacenters` property.

3.  Select the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** property.

4.  In the **Value** field, enter `false`.

5.  Select **Update**.


**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

**Related topics**  


[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

