---
title: Life cycle management of records in Service Graph Connector for GCP
description: Life cycle management in the in the Service Graph Connector for GCP monitors and updates the statuses of GCP resources throughout their entire life cycle, from creation to deletion.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-24"
reading_time_minutes: 2
breadcrumb: [Reference, GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle management of records in Service Graph Connector for GCP

Life cycle management in the in the Service Graph Connector for GCP monitors and updates the statuses of GCP resources throughout their entire life cycle, from creation to deletion.

The life cycle management process helps maintain the accuracy and integrity of data in the Configuration Management Database \(CMDB\).

In life cycle management, the record removal process involves systematically deleting obsolete or unnecessary resources. This step ensures that outdated entries are cleared, keeping the CMDB accurate and up-to-date. See [Record removal process in Service Graph Connector for GCP](sgc-cmdb-gcp-removal.md).

## Life cycle management for CIs in Service Graph Connector for GCP

The following table lists the configuration items \(CIs\) for which life cycle management is available in Service Graph Connector for GCP.

<table id="table_j2z_xvz_ncc"><thead><tr><th>

Data source

</th><th>

CMDB CI classes

</th><th>

Life cycle management available

</th></tr></thead><tbody><tr><td>

SG-GCP Organization

</td><td>

Cloud Organizations \[cmdb\_ci\_cloud\_org\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Folder

</td><td>

Google Organization Folder \[cmdb\_ci\_gcp\_folder\]

</td><td>

Yes

</td></tr><tr><td rowspan="2">

SG-GCP Project

</td><td>

Google Organization Project \[cmdb\_ci\_gcp\_project\]

</td><td>

Yes

</td></tr><tr><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Network

</td><td>

Cloud Network \[cmdb\_ci\_network\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Machine Image

</td><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

Not applicable

</td></tr><tr><td rowspan="2">

SG-GCP Subnet

</td><td>

Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

</td><td>

Yes

</td></tr><tr><td>

Google Datacenter \[cmdb\_ci\_google\_datacenter\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP Storage Volume

</td><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Storage Volume Snapshot

</td><td>

Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]

</td><td>

Yes

</td></tr><tr><td rowspan="3">

SG-GCP Security Group

</td><td>

Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

</td><td>

Yes

</td></tr><tr><td>

Network ACL \[cmdb\_ci\_network\_acl\]

</td><td>

Yes

</td></tr><tr><td>

Network ACL Rule \[cmdb\_ci\_network\_acl\_rule\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Software Inventory

</td><td>

Software \[cmdb\_ci\_spkg\] Software Instance \[cmdb\_software\_instance\]

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Yes

</td></tr><tr><td rowspan="10">

SG-GCP VM Instance

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Yes

</td></tr><tr><td>

Server \[cmdb\_ci\_server\]

</td><td>

Yes

</td></tr><tr><td>

Storage Mapping \[cmdb\_ci\_storage\_mapping\]

</td><td>

Yes

</td></tr><tr><td>

VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]

</td><td>

Yes

</td></tr><tr><td>

Block Endpoint \[cmdb\_ci\_endpoint\_block\]

</td><td>

Yes

</td></tr><tr><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td><td>

Yes

</td></tr><tr><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Yes

</td></tr><tr><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td><td>

Not applicable

</td></tr><tr><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

Yes

</td></tr><tr><td>

Availability Zone \[cmdb\_ci\_availability\_zone\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP Execute Patch Job

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td rowspan="3">

SG-GCP Hardware Type

</td><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td><td>

Not applicable

</td></tr><tr><td>

Google Datacenter \[cmdb\_ci\_google\_datacenter\]

</td><td>

Not applicable

</td></tr><tr><td>

Availability Zone \[cmdb\_ci\_availability\_zone\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP VM Hw Consolidation

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP Load Balancer Pool

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP load Balancer Pool Member

</td><td>

Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Load Balancer Health Service

</td><td>

Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Load Balancer

</td><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Load Balancer Service

</td><td>

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Cloud Database

</td><td>

Cloud DataBase \[cmdb\_ci\_cloud\_database\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Cloud Function

</td><td>

Cloud Function \[cmdb\_ci\_cloud\_function\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Cloud Object Storage

</td><td>

Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Cluster

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Node

</td><td>

Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

</td><td>

Yes

</td></tr><tr><td rowspan="4">

SG-GCP Kubernetes Pod

</td><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td><td>

Yes

</td></tr><tr><td>

Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

</td><td>

No

</td></tr><tr><td>

Docker Image \[cmdb\_ci\_docker\_image\]

</td><td>

No

</td></tr><tr><td>

Docker Container \[cmdb\_ci\_docker\_container\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Service

</td><td>

Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Namespace

</td><td>

Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Deployment

</td><td>

Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Replicaset

</td><td>

Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Cluster Roles

</td><td>

Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Cluster Role Binding

</td><td>

Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Kubernetes Node Pool

</td><td>

Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Generic Resource

</td><td>

Cloud Resource \[cmdb\_ci\_cmp\_resource\]

</td><td>

Yes

</td></tr><tr><td>

SG-GCP Annotation

</td><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP Get Patch Job

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td>

SG-GCP Generic Resource Annotation

</td><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Not applicable

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for GCP reference](sgc-cmdb-gcp-reference.md)

