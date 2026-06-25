---
title: VMware NSX-T cluster pattern-based discovery
description: Discovery and Service Mapping Patterns uses the NSX Cluster pattern to find VMware NSX-T infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/nsx-t-cluster-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 8
keywords: [NSX-T, NSX Cluster, VMware NSX, NSX discovery, NSX patterns]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# VMware NSX-T cluster pattern-based discovery

Discovery and Service Mapping Patterns uses the NSX Cluster pattern to find VMware NSX-T infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## NSX Cluster data model

The following diagram illustrates the tables and relationships that the Discovery and Service Mapping Patterns application creates when discovering NSX-T infrastructure resources.

\[Omitted image "nsx-cluster-data-model.png"\] Alt text: NSX Cluster data model

## Prerequisites

-   **Verify that the following applications are up to date**
    -   CMDB CI Class Models
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Configure a credential alias**

    For more information, see [Create an applicative credential alias for NSX-T cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-applicative-cred-alias-nsx-t.md).

-   **Verify NSX-T API access and permissions**

    Verify that the credential has sufficient permissions to execute the following NSX-T API calls:

    -   `POST /api/session/create`
    -   `GET /api/v1/cluster/status`
    -   `GET /api/v1/node`
    -   `GET /policy/api/v1/infra/segments`
    -   `GET /policy/api/v1/infra/tier-0s`
    -   `GET /policy/api/v1/infra/tier-1s`
    -   `GET /api/v1/transport-nodes`
    -   `GET /api/v1/transport-zones`
    -   `GET /api/v1/fabric/virtual-switches/`
    -   `GET /api/v1/edge-clusters`
-   **Create a serverless discovery schedule**

    For more information, see [Create a serverless schedule for NSX-T cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-nsx-t.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the NSX Cluster pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|IP address of the NSX Management Cluster.|
|IP Address \[ip\_address\]|IP address of the NSX Management Cluster.|
|Cluster Status \[cluster\_status\]|Status of the management cluster as reported by the NSX-T API.|
|Operational status \[operational\_status\]|Operational status of the resource, derived from the cluster status.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Display name of the cluster node, derived from the node's fully qualified domain name \(FQDN\).|
|ID \[nsx\_node\_id\]|Unique identifier of the NSX Manager node.|
|Fully qualified domain name \[fqdn\]|FQDN of the node.|
|Node Status \[node\_status\]|Status of the node as reported by the NSX-T API.|
|Operational status \[operational\_status\]|Operational status of the resource, derived from the node status.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

<table id="table_mgmt_cluster_node_group"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Concatenation of the cluster IP address and the group type. For example: `10.0.0.1 MANAGER`.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Group ID assigned by NSX-T.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource, derived from the group status.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr></tbody>
</table><table id="table_transport_node"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Display name of the transport node, derived from the host FQDN or virtual machine \(VM\) display name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the transport node.

</td></tr><tr><td>

Host Type \[host\_type\]

</td><td>

Type of the transport node host. For example: ESXi, KVM, or Edge.

</td></tr><tr><td>

Host Name \[host\_name\]

</td><td>

Host name of the transport node.

</td></tr><tr><td>

Host ID \[host\_id\]

</td><td>

Identifier of the host running the transport node.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

FQDN of the transport node.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the transport node.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

User-provided description of the transport node.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Display name of the transport zone.|
|Object ID \[object\_id\]|Unique identifier of the transport zone.|
|Transport Type \[transport\_type\]|Transport type of the zone. For example: OVERLAY or VLAN.|
|Forwarding Mode \[forwarding\_mode\]|Forwarding mode of the transport zone.|
|Is Default \[is\_default\]|Indicates whether this is the default transport zone.|
|Operational status \[operational\_status\]|Operational status of the resource. The value is set to Operational.|
|Install Status \[install\_status\]|Install status of the resource. The value is set to Installed.|
|Description \[short\_description\]|User-provided description of the transport zone.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Display name of the edge cluster group.|
|Object ID \[object\_id\]|Unique identifier of the edge cluster.|
|Node Type \[node\_type\]|Type of edge node in the cluster.|
|Inter Site Forwarding \[enable\_inter\_site\_forwarding\]|Indicates whether inter-site forwarding is enabled for this edge cluster.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Display name of the virtual switch.|
|Object ID \[object\_id\]|Unique identifier of the virtual switch.|
|CM Local ID \[cm\_local\_id\]|Local identifier assigned by the compute manager.|
|Origin ID \[origin\_id\]|Origin identifier of the virtual switch resource.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Display name of the gateway.|
|Object ID \[object\_id\]|Unique identifier of the gateway.|
|Tier Type \[tier\_type\]|Tier type of the gateway: Tier-0 or Tier-1.|
|HA Mode \[ha\_mode\]|High-availability mode of the gateway.|
|Failover Mode \[failover\_mode\]|Failover mode of the gateway.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Description \[short\_description\]|User-provided description of the gateway resource.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Display name of the segment.|
|Object ID \[object\_id\]|Unique identifier of the segment.|
|Operational status \[operational\_status\]|Operational status of the resource, derived from the resource state.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Description \[short\_description\]|User-provided description of the segment resource.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the transport node.|

## Dependency Views map

On the Dependency Views map, you can view discovered NSX-T cluster resources and the relationships between them.

\[Omitted image "nsx-management-cluster-ci-dependency-view.png"\] Alt text: NSX Management Cluster CI and connection on a Dependency Views map

## CI relationships

The NSX Cluster pattern creates the following relationships and references to support NSX-T cluster discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|NSX Management Cluster Node \[cmdb\_ci\_nsx\_management\_cluster\_node\]|Members::Member of|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\]|Managed by::Manages|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\]|Connects to::Connected by|NSX Segment Resource \[cmdb\_ci\_nsx\_segment\_resource\]|
|NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\] \(Tier 1\)|Connects to::Connected by|NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\] \(Tier 0\)|
|NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]|Managed by::Manages|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|NSX Management Cluster Node Group \[cmdb\_ci\_nsx\_management\_cluster\_node\_group\]|Managed by::Manages|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Management Cluster Node Group \[cmdb\_ci\_nsx\_management\_cluster\_node\_group\]|Uses::Used by|NSX Management Cluster Node \[cmdb\_ci\_nsx\_management\_cluster\_node\]|
|NSX Segment Resource \[cmdb\_ci\_nsx\_segment\_resource\]|Managed by::Manages|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Transport Zone Resource \[cmdb\_ci\_nsx\_transport\_zone\_resource\]|Managed by::Manages|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Transport Zone Resource \[cmdb\_ci\_nsx\_transport\_zone\_resource\]|Contains::Contained by|NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]|
|NSX Virtual Switch Resource \[cmdb\_ci\_nsx\_virtual\_switch\_resource\]|Managed by::Manages|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Edge Cluster Group \[cmdb\_ci\_nsx\_edge\_cluster\_group\]|Managed by::Manages|NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]|
|NSX Edge Cluster Group \[cmdb\_ci\_nsx\_edge\_cluster\_group\]|Uses::Used by|NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]|

<table id="table_ci_references"><thead><tr><th>

CI

</th><th>

Field

</th><th>

Referenced CI

</th></tr></thead><tbody><tr><td>

NSX Management Cluster Node \[cmdb\_ci\_nsx\_management\_cluster\_node\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

NSX Management Cluster Node Group \[cmdb\_ci\_nsx\_management\_cluster\_node\_group\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

NSX Segment Resource \[cmdb\_ci\_nsx\_segment\_resource\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

NSX Transport Zone Resource \[cmdb\_ci\_nsx\_transport\_zone\_resource\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

NSX Virtual Switch Resource \[cmdb\_ci\_nsx\_virtual\_switch\_resource\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

NSX Edge Cluster Group \[cmdb\_ci\_nsx\_edge\_cluster\_group\]

</td><td>

Cluster \[cluster\]

</td><td>

NSX Management Cluster \[cmdb\_ci\_nsx\_management\_cluster\]

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Configuration item \[configuration\_item\]

</td><td>

References one of the following NSX resource tables: -   NSX Segment Resource \[cmdb\_ci\_nsx\_segment\_resource\]
-   NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\]
-   NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]
-   NSX Edge Cluster Group \[cmdb\_ci\_nsx\_edge\_cluster\_group\]

</td></tr><tr><td>

External system metadata \[cmdb\_key\_value\_v2\]

</td><td>

Configuration item \[configuration\_item\]

</td><td>

References one of the following NSX resource tables: -   NSX Segment Resource \[cmdb\_ci\_nsx\_segment\_resource\]
-   NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\]
-   NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]
-   NSX Edge Cluster Group \[cmdb\_ci\_nsx\_edge\_cluster\_group\]
-   NSX Transport Zone Resource \[cmdb\_ci\_nsx\_transport\_zone\_resource\]
-   NSX Virtual Switch Resource \[cmdb\_ci\_nsx\_virtual\_switch\_resource\]

</td></tr></tbody>
</table>## Tag discovery and external system metadata

The NSX Cluster pattern collects resource tags and external system metadata. Tags are stored in the Key Value \[cmdb\_key\_value\] table. External system metadata is stored in the External system metadata \[cmdb\_key\_value\_v2\] table.

<table id="table_key_value"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

Tag name.

</td></tr><tr><td>

Value \[value\]

</td><td>

Tag value.

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References the NSX resource table associated with the tag. Possible tables:-   NSX Segment Resource \[cmdb\_ci\_nsx\_segment\_resource\]
-   NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\]
-   NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]
-   NSX Edge Cluster Group \[cmdb\_ci\_nsx\_edge\_cluster\_group\]

</td></tr></tbody>
</table><table id="table_kv_v2"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

Metadata property name.

</td></tr><tr><td>

String value \[string\_value\]

</td><td>

Value of the metadata property.

</td></tr><tr><td>

Value type \[value\_type\]

</td><td>

Data type of the metadata value.

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References the NSX resource table associated with the metadata entry. Possible tables:-   NSX Segment Resource \[cmdb\_ci\_nsx\_segment\_resource\]
-   NSX Gateway Resource \[cmdb\_ci\_nsx\_gateway\_resource\]
-   NSX Transport Node Resource \[cmdb\_ci\_nsx\_transport\_node\_resource\]
-   NSX Edge Cluster Group \[cmdb\_ci\_nsx\_edge\_cluster\_group\]
-   NSX Transport Zone Resource \[cmdb\_ci\_nsx\_transport\_zone\_resource\]
-   NSX Virtual Switch Resource \[cmdb\_ci\_nsx\_virtual\_switch\_resource\]

</td></tr></tbody>
</table>-   **[Create an applicative credential alias for NSX-T cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-applicative-cred-alias-nsx-t.md)**  
Create a credential alias and configure an applicative credential to enable the NSX Cluster pattern to authenticate with the NSX-T management cluster.
-   **[Create a serverless schedule for NSX-T cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-nsx-t.md)**  
Create a serverless discovery schedule to run the NSX Cluster pattern against a VMware NSX-T management cluster.

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

