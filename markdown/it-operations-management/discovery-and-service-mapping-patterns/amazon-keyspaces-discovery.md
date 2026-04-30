---
title: AWS Keyspaces discovery
description: The ServiceNow Discovery application uses the Amazon Keyspaces discovery pattern to find Amazon Keyspaces managed Apache Cassandra–compatible database service.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Keyspaces discovery

The ServiceNow® Discovery application uses the Amazon Keyspaces discovery pattern to find Amazon Keyspaces managed Apache Cassandra–compatible database service.

Amazon Keyspaces is a managed Apache Cassandra–compatible database service. A keyspace groups related tables that are relevant for one or more applications. It contains one or more tables and defines the replication strategy for all the tables it contains.

## Prerequisites

-   Install the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   Configure an AWS Service Account with valid credentials on the ServiceNow instance with permission to run the following APIs:
    -   `https://cassandra.{region}.amazonaws.com {Content-Type:application/x-amz-json-1.0, , X-Amz-Target: KeyspacesService.ListKeyspaces}`
    -   `https://tagging.{region}.amazonaws.com {"ResourceTypeFilters":[]}`

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

Keyspaces are stored in Cloud Databases \[cmdb\_ci\_cloud\_database\] table.

|Field|Description|
|-----|-----------|
|Amazon resource name|Name of the keyspace.|
|FQDN|Fully qualified domain name of the region where the keyspace is located.|
|Port|Port used for incoming TLS connections \(9142\).|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

