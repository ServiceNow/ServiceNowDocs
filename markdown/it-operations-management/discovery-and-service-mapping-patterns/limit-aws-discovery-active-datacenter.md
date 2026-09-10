---
title: Limit AWS discovery to datacenters with resources
description: Optimize AWS discovery by limiting it to datacenters with resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/limit-aws-discovery-active-datacenter.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Limit AWS discovery to datacenters with resources

Optimize AWS discovery by limiting it to datacenters with resources.

## Before you begin

-   Verify that you have installed Discovery and Service Mapping Patterns, starting with version 1.29.0.
-   Verify that your service account has the following IAM permissions to access the Resource Explorer API \(starting with Discovery and Service Mapping Patterns version 1.35.0\).

    |IAM permission|Coverage|
    |--------------|--------|
    |`resource-explorer-2:Search`|Partial|
    |`resource-explorer-2:Search` + `iam:CreateServiceLinkedRole`|Full|

    For more information, go to the [AWS Documentation](https://docs.aws.amazon.com/) and search for the "Getting started with Resource Explorer" article.


**Note:** Discovery and Service Mapping Patterns versions 1.29.0 through 1.32.0 used the AWS Config service instead of the Resource Explorer API to determine datacenter activity. For instructions on configuring AWS Config recorder, go to the [AWS Documentation](https://docs.aws.amazon.com/) and search for the "Recording resources in the AWS Config console" article.

Role required: discovery\_admin

## About this task

Starting with version 1.29.0, Discovery and Service Mapping Patterns introduces a new AWS datacenter discovery model that focuses discovery on datacenters with resources and excludes datacenters that don't contain resource. To limit discovery to datacenters that contain resources, set the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** MID Server property to false. For more information, see [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for the `mid.cloud.discovery.sonar.discover_all_aws_datacenters` property.

3.  Select the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** property.

4.  In the **Value** field, enter `false`.

5.  Select **Update**.


## What to do next

To exclude specific resource types from AWS datacenter discovery, configure the **sn\_itom\_pattern.discovery.aws.ldc.excluded\_resource\_types** system property with a comma-separated list of resource types to exclude \(starting with Discovery and Service Mapping Patterns version 1.35.0\). For more information, see [Exclude AWS resource types from datacenter discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/exclude-aws-resource-ldc-discovery.md).

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

**Related topics**  


[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

[Exclude AWS resource types from datacenter discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/exclude-aws-resource-ldc-discovery.md)

