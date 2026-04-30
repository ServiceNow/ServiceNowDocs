---
title: Amazon ElastiCache discovery with Patterns
description: The ServiceNow Discovery application uses the Amazon ElastiCache discovery pattern to find Redis clusters deployed as part of the ElastiCache service. ElastiCache is compatible with both Redis and Memcached, but the pattern collects information only for Redis.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon ElastiCache discovery with Patterns

The ServiceNow® Discovery application uses the Amazon ElastiCache discovery pattern to find Redis clusters deployed as part of the ElastiCache service. ElastiCache is compatible with both Redis and Memcached, but the pattern collects information only for Redis.

Amazon ElastiCache is a fully managed, in-memory caching service available on AWS.

## Prerequisites

-   Install the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   Configure an AWS Service Account with valid credentials on the ServiceNow instance with permission to run the following APIs:
    -   `https://elasticache.{region}.amazonaws.com?Action=DescribeReplicationGroups&Version=2015-02-02`
    -   `https://tagging.{region}.amazonaws.com {"ResourceTypeFilters":[]}`

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

Replication groups are stored in the Cloud Database Clusters \[cmdb\_ci\_cloud\_db\_cluster\] table and node group members are stored in the Cloud Databases \[cmdb\_ci\_cloud\_database\] table.

|Field|Description|
|-----|-----------|
|Amazon resource name|Name of the resource for each replication group and each node group member.|
|FQDN|Fully qualified domain name for each node group member.|
|Port|Port used by each node group member.|

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

