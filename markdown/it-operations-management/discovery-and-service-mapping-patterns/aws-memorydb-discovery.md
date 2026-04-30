---
title: AWS MemoryDB for Redis
description: The Discovery application uses the AWS MemoryDB for Redis pattern and extensions to find AWS MemoryDB for Redis. Discovering some of these resources requires installing the Discovery and Service Mapping Patterns application from the Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS MemoryDB for Redis

The ® Discovery application uses the AWS MemoryDB for Redis pattern and extensions to find AWS MemoryDB for Redis. Discovering some of these resources requires installing the Discovery and Service Mapping Patterns application from the ® Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

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

<table id="table_olj_wwb_x5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI \[cmdb\_ci\_cloud\_database\] 

</td></tr><tr><td>

ARN

</td><td>

The Amazon Resource Name of a single node in the cluster. The values are populated in the Object ID \[object\_id\] column.

</td></tr><tr><td>

Name

</td><td>

The name of a single node in the cluster.

</td></tr><tr><td>

FQDN

</td><td>

The Fully Qualified Domain Name of each node in the cluster.

</td></tr><tr><td>

TCP \_Port

</td><td>

The TCP port that a single node in the cluster is getting traffic from.

</td></tr><tr><td>

Type

</td><td>

The type of database is MemoryDB.

</td></tr><tr><td class="sub-head" colspan="2">

Database Cluster \[cmdb\_ci\_cloud\_db\_cluster\]

</td></tr><tr><td>

ARN

</td><td>

The Amazon Resource Name of the cluster. The values are populated in the Object ID \[object\_id\] column.

</td></tr><tr><td>

Name

</td><td>

The name of the cluster.

</td></tr><tr><td>

FQDN

</td><td>

The Fully Qualified Domain Name of the cluster.

</td></tr><tr><td>

TCP \_Port

</td><td>

The TCP port that the cluster is getting traffic from.

</td></tr></tbody>
</table><table id="table_nxq_dcc_x5b"><thead><tr><th>

CI

</th><th>

Relationship Type

</th><th>

CI

</th></tr></thead><tbody><tr><td>

\[cmdb\_ci\_appl\]

</td><td>

Extends from

</td><td>

\[cmdb\_ci\]

</td></tr><tr><td>

\[cmdb\_ci\_cloud\_database\]

</td><td>

Extends from

</td><td>

\[cmdb\_ci\_db\_instance\]

</td></tr><tr><td>

\[cmdb\_ci\_cloud\_db\_cluster\]

</td><td>

Cluster::Cluster of

</td><td>

\[cmdb\_ci\_cloud\_db\_cluster\]

</td></tr><tr><td>

\[cmdb\_ci\_cloud\_db\_cluster\]

</td><td>

Reference only

 \(configuration\_item\)

</td><td>

\[cmdb\_key\_value\]

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

**Related topics**  


[Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md)

[Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

