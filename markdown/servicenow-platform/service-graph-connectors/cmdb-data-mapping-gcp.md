---
title: Data mapping for Service Graph Connector for GCP
description: Data from the GCP data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/cmdb-data-mapping-gcp.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-01"
reading_time_minutes: 7
breadcrumb: [GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for GCP

Data from the GCP data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for GCP

When you complete setting up the connection, you can configure the integration to periodically pull data from the GCP application.

The following table lists the data sources, the staging tables, the target tables as the CMDB CI classes, and the resource types imported for a GCP project.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

CMDB CI classes

</th><th>

Resource types

</th></tr></thead><tbody><tr><td>

SG-GCP Organization

</td><td>

SG-GCP Organization \[sn\_gcp\_integ\_sg\_gcp\_organization\]

</td><td>

[Cloud Organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Organization

</td></tr><tr><td>

SG-GCP Folder

</td><td>

SG-GCP Folder \[sn\_gcp\_integ\_sg\_gcp\_folder\]

</td><td>

[Google Organization Folder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Folder

</td></tr><tr><td>

SG-GCP Project

</td><td>

SG-GCP Project \[sn\_gcp\_integ\_sg\_gcp\_project\]

</td><td>

[Google Organization Project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Project

</td></tr><tr><td>

SG-GCP Network

</td><td>

SG-GCP Network \[sn\_gcp\_integ\_sg\_gcp\_network\]

</td><td>

[Cloud Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Network

</td></tr><tr><td>

SG-GCP Machine Image

</td><td>

SG-GCP Machine Image \[sn\_gcp\_integ\_sg\_gcp\_machine\_image\]

</td><td>

[Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

MachineImage

</td></tr><tr><td>

SG-GCP Subnet

</td><td>

SG-GCP Subnet \[sn\_gcp\_integ\_sg\_gcp\_subnet\]

</td><td>

[Cloud Subnet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Subnetwork

</td></tr><tr><td>

SG-GCP Storage Volume

</td><td>

SG-GCP Storage Volume \[sn\_gcp\_integ\_sg\_gcp\_storage\_volume\]

</td><td>

[Storage Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Cloud Disk Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Availability Zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Disk

</td></tr><tr><td>

SG-GCP Storage Volume Snapshot

</td><td>

SG-GCP Storage Volume Snapshot \[sn\_gcp\_integ\_sg\_gcp\_storage\_vol\_snapshot\]

</td><td>

[Storage Volume Snapshot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Snapshot

</td></tr><tr><td>

SG-GCP Security Group

</td><td>

SG-GCP Security Group \[sn\_gcp\_integ\_sg\_gcp\_security\_group\]

</td><td>

[Compute Security Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Network ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Network ACL Rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Firewall

</td></tr><tr><td>

SG-GCP Software Inventory

</td><td>

SG-GCP Software Inventory \[sn\_gcp\_integ\_sg\_gcp\_software\_inventory\]

</td><td>

When the Software Asset Management \(SAM\) application isn't installed:

 [Software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

 [Software Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

 When the SAM application is installed: [Software Installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Instance

</td></tr><tr><td>

SG-GCP VM Instance

</td><td>

SG-GCP VM Instance \[sn\_gcp\_integ\_sg\_gcp\_vm\_instance\]

</td><td>

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Availability Zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Cloud Mgmt Network Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Storage Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Storage Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[VNIC Endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Block Endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Instance

</td></tr><tr><td>

SG-GCP Execute Patch Job

</td><td>

SG-GCP Execute Patch Job \[sn\_gcp\_integ\_sg\_gcp\_execute\_patch\_job\]

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP Hardware Type

</td><td>

SG-GCP Hardware Type \[sn\_gcp\_integ\_sg\_gcp\_hardware\_type\]

</td><td>

[Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Availability Zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

MachineType

</td></tr><tr><td>

SG-GCP VM Hw Consolidation

</td><td>

SG-GCP VM Hw Consolidation \[sn\_gcp\_integ\_sg\_gcp\_vm\_hw\_consolidation\]

</td><td>

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

None

</td></tr><tr><td>

SG-GCP Load Balancer Pool

</td><td>

SG-GCP Load Balancer Pool \[sn\_gcp\_integ\_sg\_gcp\_load\_balancer\_pool\]

</td><td>

[Load Balancer Pool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

TargetPool

</td></tr><tr><td>

SG-GCP Load Balancer Pool Member

</td><td>

SG-GCP Load Balancer Pool Member \[sn\_gcp\_integ\_sg\_gcp\_load\_balancer\_pool\_member\]

</td><td>

[Load Balancer Pool Member](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

TargetPool

</td></tr><tr><td>

SG-GCP Load Balancer Health Service

</td><td>

SG-GCP Load Balancer Health Service\[sn\_gcp\_integ\_sg\_gcp\_load\_balancer\_health\_service\]

</td><td>

[Cloud Load Balancer Health Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

HealthCheck

</td></tr><tr><td>

SG-GCP Load Balancer

</td><td>

SG-GCP Load Balancer \[sn\_gcp\_integ\_sg\_gcp\_load\_balancer\]

</td><td>

[Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

BackendService

</td></tr><tr><td>

SG-GCP Load Balancer Service

</td><td>

SG-GCP Load Balancer Service \[sn\_gcp\_integ\_sg\_gcp\_load\_balancer\_service\]

</td><td>

[Load Balancer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

ForwardingRule

</td></tr><tr><td>

SG-GCP Cloud Database

</td><td>

SG-GCP Cloud Database \[sn\_gcp\_integ\_sg\_gcp\_cloud\_database\]

</td><td>

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Instance

</td></tr><tr><td>

SG-GCP Cloud Function

</td><td>

SG-GCP Cloud Function \[sn\_gcp\_integ\_sg\_gcp\_cloud\_function\]

</td><td>

[Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Function

</td></tr><tr><td>

SG-GCP Cloud Object Storage

</td><td>

SG-GCP Cloud Object Storage \[sn\_gcp\_integ\_sg\_gcp\_cloud\_object\_storage\]

</td><td>

[Cloud Object Storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Google Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Buckets

</td></tr><tr><td>

SG-GCP Kubernetes Cluster

</td><td>

SG-GCP Kubernetes Cluster \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_cluster\]

</td><td>

[Kubernetes Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Cluster

</td></tr><tr><td>

SG-GCP Kubernetes Node

</td><td>

SG-GCP Kubernetes Node \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_node\]

</td><td>

[Kubernetes Node](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Node

</td></tr><tr><td>

SG-GCP Kubernetes Pod

</td><td>

SG-GCP Kubernetes Pod \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_pod\]

</td><td>

[Kubernetes Pod](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Kubernetes Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Docker Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Docker Container](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Pod

</td></tr><tr><td>

SG-GCP Kubernetes Service

</td><td>

SG-GCP Kubernetes Service \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_service\]

</td><td>

[Kubernetes Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Service

</td></tr><tr><td>

SG-GCP Kubernetes Namespace

</td><td>

SG-GCP Kubernetes Namespace \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_namespace\]

</td><td>

[Kubernetes Namespace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Namespace

</td></tr><tr><td>

SG-GCP Kubernetes Deployment

</td><td>

SG-GCP Kubernetes Deployment \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_deployment\]

</td><td>

[Kubernetes Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Deployment

</td></tr><tr><td>

SG-GCP Kubernetes Replicaset

</td><td>

SG-GCP Kubernetes Replicaset \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_replicaset\]

</td><td>

[Kubernetes ReplicaSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

ReplicaSet

</td></tr><tr><td>

SG-GCP Kubernetes Cluster Roles

</td><td>

SG-GCP Kubernetes Cluster Roles \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_cluster\_role\]

</td><td>

[Kubernetes Cluster Role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

ClusterRole

</td></tr><tr><td>

SG-GCP Kubernetes Cluster Role Binding

</td><td>

SG-GCP Kubernetes Cluster Role Binding \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_cluster\_role\_binding\]

</td><td>

[Kubernetes Cluster Role Binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

ClusterRoleBinding

</td></tr><tr><td>

SG-GCP Kubernetes Node Pool

</td><td>

SG-GCP Kubernetes Node Pool \[sn\_gcp\_integ\_sg\_gcp\_kubernetes\_node\_pool\]

</td><td>

[Kubernetes Node Pool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[SG-GCP Extension Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

NodePool

</td></tr><tr><td>

SG-GCP Generic Resource

</td><td>

SG-GCP Generic Resource \[sn\_gcp\_integ\_sg\_gcp\_generic\_resource\]**Note:** The SG-GCP Generic Resource data source only works with a service account that has organization-level access.

</td><td>

[Cloud Resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Resource

</td></tr><tr><td>

SG-GCP Annotation

</td><td>

SG-GCP Annotation \[sn\_gcp\_integ\_sg\_gcp\_annotation\]

</td><td>

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Annotation

</td></tr><tr><td>

SG-GCP Get Patch Job

</td><td>

SG-GCP Get Patch Job \[sn\_gcp\_integ\_sg\_gcp\_get\_patch\_job\]

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP Generic Resource Annotation

</td><td>

SG-GCP Generic Resource Annotation \[sn\_gcp\_integ\_sg\_gcp\_generic\_resource\_annotation\]

</td><td>

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

</td><td>

Annotation

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from a GCP project, see [CMDB classes targeted in Service Graph Connector for GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

Additional information about GCP data sources:

-   The SG-GCP Annotation data source populates all labels and tags associated with GCP supported resources to the [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md) table.
-   The SG-GCP Generic Resource Annotation data source populates the tags and labels for Generic resources to the [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md) table from Service Graph Connector for GCP version 1.10.0.
-   The basic information about a GCP resource is stored in the SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\] table.
-   After all the data sources are executed, the Server \[cmdb\_ci\_server\] class is updated with the class entry, and then based on the Windows or Linux class, the records are created in the Windows Server \[cmdb\_ci\_win\_server\] and Linux Server \[cmdb\_ci\_linux\_server\] classes, respectively.
-   The SG-GCP Generic Resource data source imports data for resources that are categorized as `Generic` in the Service Graph Resource Inclusion Whitelist \[sn\_cmdb\_int\_util\_service\_graph\_resource\_inclusion\_whitelist\] table.

-   For any discovered resources that are deleted after pulling data, the Service Graph Connector for GCP automatically updates the **Install Status** field of the associated CMDB CI classes to indicate any retired or deleted records. For more information, see [Life cycle management of records in Service Graph Connector for GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-lc.md) and [Record removal process in Service Graph Connector for GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-removal.md).
-   When the **sn\_itom\_pattern.use a single hardware type for cloud data centers** system property is set to `true`, hardware type data is added to the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table, instead of being added to the Hardware Type \[cmdb\_ci\_compute\_template\] table from Service Graph Connector for GCP version 1.9.0. For more information, see the [Service Graph Connector For GCP - Migrating to a new hardware type model \[KB1899584\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1899584) article in the Now Support Knowledge Base.
-   When the **sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image** system property is set to `true`, image type data is added to the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table, instead of being added to the Image \[cmdb\_ci\_os\_template\] table from Service Graph Connector for GCP version 1.9.0. For more information, see the [Service Graph Connector For GCP - Migrating to a new Cloud OS Image model \[KB1983751\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1983751) article in the Now Support Knowledge Base.
-   The list API calls return only the information that is required to make batch calls and not the entire resource response from Service Graph Connector for GCP version 1.9.0.
-   Parallel data loading is enabled for the SG-GCP Annotation, SG-GCP Generic Resource,and SG-GCP Generic Resource Annotation data sources.
-   You can configure the **AppScript Folder IDs** connection property to exclude AppScript folder information from imports starting from Service Graph Connector for GCP version 1.10.0. For more information, see [Service Graph Connector for GCP properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-sgc-gcp-props.md).
-   The SG-GCP Software Inventory scheduled import runs before the SG-GCP VM Instance scheduled import from Service Graph Connector for GCP version 1.10.0. The SG-GCP Software Inventory scheduled job populates the operating system information for the Server records, which determines the script that needs to be run for deep discovery \(Shell script for Linux VMs or PowerShell script for Windows VMs\).
-   The SG-GCP Get Patch Job scheduled import supports deep discovery by running commands on VMs from Service Graph Connector for GCP version 1.10.0. For information about deep discovery for the Service Graph Connector for GCP, see the [Enabling deep discovery for Service Graph Connector for GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-gcp-deep-discovery.md) article in the Now Support Knowledge Base.

## Related content

[CMDB classes targeted in Service Graph Connector for GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-gcp-classes.md)

[Service Graph Connector for GCP properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-sgc-gcp-props.md)

