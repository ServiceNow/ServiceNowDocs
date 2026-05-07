---
title: AWS MemoryDB for Redis discovery with Patterns
description: The Discovery application uses the Amazon AWS MemoryDB pattern and extensions to find AWS MemoryDB for Redis. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS MemoryDB for Redis discovery with Patterns

The ® Discovery application uses the Amazon AWS MemoryDB pattern and extensions to find AWS MemoryDB for Redis. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Configured AWS Credentials**

    On your instance, configure credentials of type **AWS Credentials**. For more information, see [Access setup for AWS service accounts](../../it-operations-management/concept/access-aws-accounts.md).

-   **Configured Cloud service account**

    Configure the AWS service account valid in the ServiceNow instance. For more information, see [Set up AWS service accounts.](../../it-operations-management/concept/setup-aws-service-accounts.md)

-   **Configured user permissions to execute the list AWS MemoryDB for Redis API calls**

    Provide the user permission to run the following API:

    -   https://memory-db.\{region\}.amazonaws.com?Action=DescribeClusters&amp;ShowShardDetails=true
    -   https://memory-db.\{region\}.amazonaws.com? Action=ListTags&amp;ResourceArn=\{arn\}
    For more information, see [Amazon AWS Cloud components discovery using patterns.](../../discovery/reference/data-discovered-aws-patterns.md)

-   **Configured Cloud Discovery schedule**

    Create a cloud application schedule for discovering AWS datacenters. Set **Discovery** to **Cloud discovery**. For more information, see: [Create schedules for discovering cloud resources in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md)


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected during AWS MemoryDB for Redis horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS MemoryDB pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The Amazon Resource Name of a single node in the cluster.|
|Name \[name\]|The name of a single node in the cluster.|
|Fully qualified domain name \[fqdn\]|The Fully Qualified Domain Name of each node in the cluster.|
|TCP port\(s\) \[tcp\_port\]|The TCP port that a single node in the cluster is getting traffic from.|
|Type \[type\]|The type of database. Value is set to **memorydb**.|

|Field|Description|
|-----|-----------|
|Cluster ID \[cluster\_id\]|The Amazon Resource Name of the cluster.|
|Name \[name\]|The name of the cluster.|
|Fully qualified domain name \[fqdn\]|The Fully Qualified Domain Name of the cluster.|
|TCP port\(s\) \[tcp\_port\]|The TCP port that the cluster is getting traffic from.|

## CI relationships

The AWS MemoryDB for Redis pattern creates the following relationships and references to support AWS MemoryDB for Redis discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Cluster of::Cluster|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|

## AWS tag discovery

The AWS MemoryDB for Redis pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\] table.|

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

**Related topics**  


[Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md)

[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

