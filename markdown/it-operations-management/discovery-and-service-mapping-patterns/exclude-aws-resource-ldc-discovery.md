---
title: Exclude AWS resource types from datacenter discovery
description: You can configure which AWS resource types to exclude from AWS datacenter discovery, to avoid triggering discovery patterns in regions with only default resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/exclude-aws-resource-ldc-discovery.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 1
keywords: [AWS resource types, datacenter discovery, passive datacenter, Resource Explorer]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Exclude AWS resource types from datacenter discovery

You can configure which AWS resource types to exclude from AWS datacenter discovery, to avoid triggering discovery patterns in regions with only default resources.

## Before you begin

-   Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.
-   Discover only datacenters with resources by setting the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** MID Server property to **false**. For more information, see [Limit AWS discovery to datacenters with resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/limit-aws-discovery-active-datacenter.md).

Role required: discovery\_admin

## About this task

Some resource types, such as default Virtual Private Cloud \(VPC\) and security groups, exist in all regions regardless of whether workloads are deployed there. You can use the **sn\_itom\_pattern.discovery.aws.ldc.excluded\_resource\_types** system property to exclude these resource types. The default value of the property is empty, which includes all supported resource types in the query. Excluding these resources gives a more accurate view of which datacenters are active.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for the `sn_itom_pattern.discovery.aws.ldc.excluded_resource_types` property.

3.  Select the **sn\_itom\_pattern.discovery.aws.ldc.excluded\_resource\_types** property.

4.  In the **Value** field, enter a comma-separated list of AWS resource type identifiers to exclude.

    For example: `ec2:vpc,ec2:security-group`.

5.  Select **Update**.


**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

**Related topics**  


[Limit AWS discovery to datacenters with resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/limit-aws-discovery-active-datacenter.md)

[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

