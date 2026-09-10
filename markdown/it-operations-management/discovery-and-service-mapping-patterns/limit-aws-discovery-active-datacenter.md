---
title: Limit AWS discovery to datacenters with resources
description: Optimize AWS discovery by limiting it to datacenters with resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery-and-service-mapping-patterns/limit-aws-discovery-active-datacenter.html
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [AWS cloud components, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Limit AWS discovery to datacenters with resources

Optimize AWS discovery by limiting it to datacenters with resources.

## Before you begin

-   Verify that you have installed Discovery and Service Mapping Patterns, starting with version 1.29.0.
-   Verify your service account has the following role permissions to access Config API:
    -   `config:GetDiscoveredResourceCounts`
    -   `config:DescribeConfigurationRecorderStatus`
-   Verify AWS Config recorder is enabled and configured to record the all resource types.

    For instructions on configuring AWS Config recorder, go to the [AWS Documentation](https://docs.aws.amazon.com/) and search for the "Recording resources in the AWS Config console" article.


Role required: discovery\_admin

## About this task

Starting with version 1.29.0, Discovery and Service Mapping Patterns introduces a new AWS datacenter discovery model that focuses discovery on datacenters with resources and excludes datacenters that don't contain resource. To limit discovery to datacenters that contain resources, set the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** MID Server property to false. For more information, see [Amazon AWS Cloud components discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for the `mid.cloud.discovery.sonar.discover_all_aws_datacenters` property.

3.  Select the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** property.

4.  In the **Value** field, enter `false`.

5.  Select **Update**.


**Parent Topic:**[Amazon AWS Cloud components discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

**Related topics**  


[Amazon AWS Cloud components discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

