---
title: Data collected for Amazon AWS Cloud Discovery
description: Discovery collects information about cloud resources in AWS datacenters. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Patterns]
breadcrumb: [Cloud resource discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Data collected for Amazon AWS Cloud Discovery

Discovery collects information about cloud resources in AWS datacenters. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date.**
    -   Discovery and Service Mapping Patterns.
    -   CMDB CI Class Models.
    -   Visibility Content.
-   **Configure a discovery schedule**

    [Create a discovery schedule in Cloud Discovery Workspace](../task/cloud-operations-disco-create-schedule.md)


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected for AWS Cloud Discovery

The following tables show examples of data collected during AWS Cloud Discovery.

|Label|Field Name|
|-----|----------|
|Name|name|
|Region|region|
|Object ID|object\_id|

|Label|Field Name|
|-----|----------|
|Name|name|

|Label|Field Name|
|-----|----------|
|Name|name|
|State|state|
|Object ID|object\_id|
|CPUs|cpus|
|Disks|disks|
|Memory|memory|
|Network adapters|nics|
|VM Instance ID|vm\_inst\_id|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|State|state|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|Guest OS|guest\_os|
|Root device type|root\_device\_type|
|Image source|image\_source|
|Image type|image\_type|

|Label|Field Name|
|-----|----------|
|Name|name|
|vCPUs|vcpus|
|Memory MB|memory\_mb|
|Local Storage GB|local\_storage\_gb|

|Label|Field Name|
|-----|----------|
|Name|name|
|State|state|
|Object ID|object\_id|
|Storage type|storage\_type|
|Size|size|

|Label|Field Name|
|-----|----------|
|Name|name|
|State\*|state|
|CIDR\*|cidr|

\*Not found on VMware vCenter networks.

|Label|Field Name|
|-----|----------|
|Name|name|
|Status|status|
|CIDR|cidr|

|Label|Field Name|
|-----|----------|
|Name|name|
|Netmask|netmask|
|MAC Manufacturer|mac\_manufacturer|
|Status|install\_status|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|State|state|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|State|state|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|Public IP address|public\_ip\_address|
|Public DNS|public\_dns|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|Sku Name|sku\_name|
|State|state|

|Label|Field name|
|-----|----------|
|DNS Alias \[cmdb\_ci\_dns\_alias\]|
|Name|name|
|Category|category|
|Status|status|
|DNS name \[cmdb\_ci\_dns\_name\]|
|Name|name|
|IP address|ip\_address|

<table id="table_wbh_q4s_mbb"><thead><tr><th>

Label

</th><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

name

</td><td>

The name of the database that you created in AWS.

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td><td>

This is also the name of the database.

</td></tr><tr><td>

Type

</td><td>

Type

</td><td>

The type of database you created.

</td></tr><tr><td>

Fully qualified domain name

</td><td>

fqdn

</td><td>

The FQDN that AWS assigned to your database. An example format for AWS is as follows: `database-name.{random-number}.{datacenter}.rds.amazonaws.com`

</td></tr><tr><td>

State

</td><td>

state

</td><td>

The state of the database: whether it is Available or Terminated.

</td></tr><tr><td>

TCP port\(s\)

</td><td>

tcp\_port

</td><td>

The TCP port that the database communicates through.

</td></tr><tr><td>

Category

</td><td>

category

</td><td>

The instance class of the database, for example: db.t2.micro.

</td></tr><tr><td>

Automated Backups

</td><td>

automated\_backup

</td><td>

Indicates whether automated backups are enabled and the retention period.

</td></tr></tbody>
</table>|Label|Field Name|
|-----|----------|
|Name|name|
|Install status|install\_status|
|Vendor|vendor|
|Fully qualified domain name|fqdn|
|Operational status|operational\_status|
|State|state|

|Label|Field Name|Description|
|-----|----------|-----------|
|Name|name|The name of the kube-controller-manager leader.|
|Port|port|The identifier for the Kubernetes apiserver port.|
|Kubernetes UID|k8s\_uid|The unique identifier for the Kubernetes Cluster.|
|Vendor|vendor|The vendor of the Kubernetes Cluster.|
|Fully qualified domain name|fqdn|The fully qualified domain name of the Kubernetes apiserver.|

**Parent Topic:**[Cloud resource discovery](cloud-discovery-collected-data.md)

**Related topics**  


[Amazon AWS Cloud components discovery using patterns](data-discovered-aws-patterns.md)

[Service Graph Connector for AWS](https://www.servicenow.com/docs/access?context=cmdb-integration-aws-sg&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Agent Client Collector for Visibility - Content](../../agent-client-collector/concept/acc-visibility-landing-page.md)

