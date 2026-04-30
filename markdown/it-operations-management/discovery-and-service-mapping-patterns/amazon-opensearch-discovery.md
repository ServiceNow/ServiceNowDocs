---
title: AWS OpenSearch discovery with Patterns
description: The ServiceNow Discovery application uses the Amazon OpenSearch discovery pattern to find Amazon OpenSearch service domains.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS OpenSearch discovery with Patterns

The ServiceNow® Discovery application uses the Amazon OpenSearch discovery pattern to find Amazon OpenSearch service domains.

OpenSearch is an open-source search and analytics engine for use cases such as log analytics, real-time application monitoring, and clickstream analysis. OpenSearch operates as a cluster of nodes that are abstracted from the end user. An OpenSearch service domain is synonymous with an OpenSearch cluster. Domains are clusters with settings, instance types, instance counts, and storage resources.

## Prerequisites

-   Install the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   Configure an AWS Service Account with valid credentials on the ServiceNow instance with permission to run the following APIs:
    -   `https://es.{region}.amazonaws.com/2021-01-01/domain`
    -   `https://es.{region}.amazonaws.com/2021-01-01/opernsearch/domain-info{"DomainNames":[]}`
    -   `https://tagging.{region}.amazonaws.com {"ResourceTypeFilters":[]}`

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

OpenSearch service domains are stored in Cloud Databases \[cmdb\_ci\_cloud\_database\] table.

|Field|Description|
|-----|-----------|
|Amazon resource name|Name of the service domain.|
|FQDN|Fully qualified domain name of the region where the keyspace is located.|

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

