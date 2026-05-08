---
title: Amazon DB cluster discovery with Patterns
description: ServiceNow Discovery uses the AWS DB cluster discovery pattern to find and map Aurora DB clusters, Aurora Serverless resources, Amazon Neptune DB instances, and Amazon DocumentDB instances. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon DB cluster discovery with Patterns

ServiceNow Discovery uses the AWS DB cluster discovery pattern to find and map Aurora DB clusters, Aurora Serverless resources, Amazon Neptune DB instances, and Amazon DocumentDB instances. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The discovered DB clusters form new relationships with the DB Instances discovered by the AWS Relational Database Service pattern. Therefore, the AWS DB cluster pattern is triggered after the AWS Relational Database Service pattern during discovery. For further information, see [Amazon Relational Database Service \(Amazon RDS\) discovery with Patterns](aws-rds-discovery.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Install the Discovery and Service Mapping Patterns application \(version 1.0.75\) from the ServiceNow Store.
-   On the ServiceNow AI Platform, configure AWS credentials, using a secret key and an access key.
-   [Create a service account](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md). Set the **Account ID** to the Amazon account ID to which RDS belongs. Use the Account ID as it appears in the AWS Management Console.
-   Set read-only permissions for these REST APIs:
    -   https://rds.&lt;REGION&gt;.amazonaws.com/?Action=DescribeDBInstances
    -   https://rds.&lt;REGION&gt;.amazonaws.com/?Action=DescribeDBClusters
    -   https://rds.&lt;REGION&gt;.amazonaws.com/?Action=DescribeDBInstances&amp;DBInstanceIdentifier=&lt;input\_object\_id&gt; for events discovery
    -   https://tagging.&lt;REGION&gt;.amazonaws.com/ for tags discovery
-   For Cloud Discovery, download the Discovery and Service Mapping Patterns from the ServiceNow Store.
-   When installing the MID Server, ensure that the host machine meets or exceeds the MID Server system requirements published on the ServiceNow documentation site.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

<table id="table_csg_wcy_vjb"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Cloud Database Cluster \[cmdb\_ci\_cloud\_db\_cluster\]

</td></tr><tr><td>

Cluster ID \[cluster\_id\]

</td><td>

Contains a user-supplied DB cluster identifier. This identifier is the unique key that identifies a DB cluster.

</td></tr><tr><td>

Name \[name\]

</td><td>

Contains the name of the initial database of the DB cluster that was provided on creation. If a name was not specified, the cluster identifier is used as the name. This name is returned for the life of the DB cluster.​

</td></tr><tr><td>

FQDN \[fqdn\]

</td><td>

Specifies the connection endpoint for the primary instance of the DB cluster.​

</td></tr><tr><td>

TCP Port \[tcp\_port\]

</td><td>

Port of the database endpoint.​

</td></tr><tr><td>

Vendor \[vendor\]

</td><td>

The vendor, Amazon.

</td></tr><tr><td>

Cluster Status \[cluster\_status\]

</td><td>

Specifies the current state of this DB cluster.​

</td></tr><tr><td>

Operational Status \[operational\_status\]

</td><td>

Status of the database, ”available” if operational.

</td></tr><tr><td class="sub-head" colspan="2">

Cloud Database \[cmdb\_ci\_cloud\_database\]

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The instance identifier for this member of the DB cluster.​**Note:** For Database Instances, this table is populated with only the object\_id attribute. This attribute is required for identification of the Cloud Database CIs, to ensure relationships between the CIs and the Cloud Database Clusters can be made.​

</td></tr><tr><td>

Name \[name\]

</td><td>

Contains the name of the initial database of the DB cluster that was provided on creation. If a name was not specified, the cluster identifier is used as the name. This name is returned for the life of the DB cluster.​

</td></tr><tr><td>

FQDN \[fqdn\]

</td><td>

Specifies the connection endpoint for the primary instance of the DB cluster.​

</td></tr><tr><td>

TCP Port \[tcp\_port\]

</td><td>

Port of the database endpoint.

</td></tr><tr><td>

Vendor \[vendor\]

</td><td>

The vendor, Amazon.

</td></tr><tr><td>

Operational Status \[operational\_status\]

</td><td>

Status of the database, ”available” if operational.

</td></tr><tr><td class="sub-head" colspan="2">

IP Address \[cmdb\_ci\_ip\_address\]

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the Cloud DB Cluster Writer endpoint.

</td></tr><tr><td>

Name \[name\]

</td><td>

The IP address.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Address of the database endpoint. The DNS name.

</td></tr><tr><td>

Netmask \[netmask\]

</td><td>

IP netmask \[0.0.0.0\].​

</td></tr></tbody>
</table>## CI relationships

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_cloud\_db\_cluster|Cluster off::Cluster​|cmdb\_ci\_cloud\_database|
|cmdb\_ci\_cloud\_database​|Hosted on::Hosts​|cmdb\_ci\_aws\_datacenter|
|cmdb\_ci\_cloud\_db\_cluster​|Owns::Owned by​|cmdb\_ci\_ip\_address​|
|cmdb\_ci\_cloud\_database|Owns::Owned by​|cmdb\_ci\_ip\_address​|
|cmdb\_key\_value|Reference only​|cmdb\_ci\_cloud\_db\_cluster​|
|cmdb\_key\_value|Reference only​|cmdb\_ci\_cloud\_database|

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

