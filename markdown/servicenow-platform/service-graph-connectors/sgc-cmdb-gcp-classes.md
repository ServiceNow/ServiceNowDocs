---
title: CMDB classes targeted in Service Graph Connector for GCP
description: When you complete setting up the connection, you can configure the integration to periodically pull data from a GCP project. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 21
breadcrumb: [GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for GCP

When you complete setting up the connection, you can configure the integration to periodically pull data from a GCP project. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Availability Zone \[cmdb\_ci\_availability\_zone\]

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Block Endpoint \[cmdb\_ci\_endpoint\_block\]

The following attributes in the Block Endpoint \[cmdb\_ci\_endpoint\_block\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|Name|name|
|Install Status|install\_status|
|Operational status|operational\_status|

## Cloud DataBase \[cmdb\_ci\_cloud\_database\]

The following attributes in the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|TCP port\(s\)|tcp\_port|
|CPU Count|cpu\_count|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|IP Address|ip\_address|
|Memory Size \(GB\)|memory\_size|
|Node Count|node\_count|
|Operational status|operational\_status|
|State|state|
|Type|type|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Disk Type \[cmdb\_ci\_disk\_type\]

The following attributes in the Cloud Disk Type \[cmdb\_ci\_disk\_type\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Disk Type \[cmdb\_ci\_disk\_type\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Disk Type \[cmdb\_ci\_disk\_type\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Function \[cmdb\_ci\_cloud\_function\]

The following attributes in the Cloud Function \[cmdb\_ci\_cloud\_function\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|CodeSha256|codesha256|
|Function Last Modified|function\_last\_modified|
|Install Status|install\_status|
|Language|language|
|Operational status|operational\_status|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

The following attributes in the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]

The following attributes in the Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Healthy threshold|healthy\_threshold|
|Install Status|install\_status|
|Interval in seconds|check\_interval\_sec|
|Monitor type protocol|monitor\_type|
|Operational status|operational\_status|
|Port|port|
|Request path|request\_path|
|Timeout in seconds|timeout\_sec|
|Unhealthy threshold|unhealthy\_threshold|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

The following attributes in the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Name|name|
|Object ID|object\_id|
|Public IP|public\_ip|
|Install Status|install\_status|
|Operational status|operational\_status|
|Private IP|private\_ip|
|Configuration Item|cmdb\_ci|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Reference|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Cloud Network \[cmdb\_ci\_network\]

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Description|short\_description|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Network ACL \[cmdb\_ci\_network\_acl\]|
|Cloud Network \[cmdb\_ci\_network\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

The following attributes in the Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Cloud Provider|cloud\_provider|
|Install Status|install\_status|
|Operational status|operational\_status|
|Service Name|service\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Organizations \[cmdb\_ci\_cloud\_org\]

The following attributes in the Cloud Organizations \[cmdb\_ci\_cloud\_org\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Time|time|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Resource \[cmdb\_ci\_cmp\_resource\]

The following attributes in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Description|short\_description|
|Install status|install\_status|
|Operational status|operational\_status|
|Resource type|resource\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Name|name|
|Object ID|object\_id|
|Datacenter Type|datacenter\_type|
|Install status|install\_status|
|Operational status|operational\_status|
|Organization Id|organization\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

The following attributes in the Cloud Subnet \[cmdb\_ci\_cloud\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Available IP Count|available\_ip\_count|
|Broadcast Address|broadcast\_address|
|CIDR|cidr|
|Gateway|gateway|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|
|Subnet Mask|subnet\_mask|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

The following attributes in the Compute Security Group \[cmdb\_ci\_compute\_security\_group\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Reference|Key Value \[cmdb\_key\_value\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Docker Container \[cmdb\_ci\_docker\_container\]

The following attributes in the Docker Container \[cmdb\_ci\_docker\_container\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Container id|container\_id|
|Command|command|
|Container created|container\_created\_at|
|Image id|image\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Status|status|

## Docker Image \[cmdb\_ci\_docker\_image\]

The following attributes in the Docker Image \[cmdb\_ci\_docker\_image\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Image id|image\_id|
|Name|name|

## Google Datacenter \[cmdb\_ci\_google\_datacenter\]

The following attributes in the Google Datacenter \[cmdb\_ci\_google\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Region|region|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Google Organization Folder \[cmdb\_ci\_gcp\_folder\]

The following attributes in the Google Organization Folder \[cmdb\_ci\_gcp\_folder\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Parent|parent\_ci|
|Parent Id|parent\_id|
|Parent Type|parent\_type|
|Time|time|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|
|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|Reference|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|
|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|Reference|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|

## Google Organization Project \[cmdb\_ci\_gcp\_project\]

The following attributes in the Google Organization Project \[cmdb\_ci\_gcp\_project\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Operational status|operational\_status|
|Discovery credentials|discovery\_credentials|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Parent|parent\_ci|
|Parent Id|parent\_id|
|Parent Type|parent\_type|
|Project Id|project\_id|
|Project Number|project\_number|
|Status|status|
|Time|time|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Organization Project \[cmdb\_ci\_gcp\_project\]|Reference|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|
|Google Organization Project \[cmdb\_ci\_gcp\_project\]|Reference|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|

## Hardware Type \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Class|className|
|Description|short\_description|
|Local Storage GB|local\_storage\_gb|
|Memory MB|memory\_mb|
|vCPUs|vcpus|
|Zone|zone|

**Note:** If the **sn\_itom\_pattern.use a single hardware type for cloud data centers** system property is set to `true`, the **className** is set to Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]. If the property is set to `false`, the **className** is set to Hardware Type \[cmdb\_ci\_compute\_template\].

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|

## Image \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Class|className|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Operational status|operational\_status|

**Note:** If the **sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image** system property is set to `true`, the **className** is set to Cloud Image \[cmdb\_ci\_cloud\_os\_image\]. If the property is set to `false`, the **className** is set to Image \[cmdb\_ci\_os\_template\].

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Image \[cmdb\_ci\_os\_template\]|Reference|Key Value \[cmdb\_key\_value\]|
|Image \[cmdb\_ci\_os\_template\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Install Status|install\_status|
|IP version|ip\_version|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Key Value \[cmdb\_key\_value\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

The tags and labels associated with the following CI classes are populated in the Key Value \[cmdb\_key\_value\] table.

|CMDB CI classes|Label populated|Tag populated|
|---------------|---------------|-------------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Yes|Yes|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Yes|Yes|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|No|Yes|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|No|Yes|
|Cloud Network \[cmdb\_ci\_network\]|No|Yes|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Yes|Yes|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|No|Yes|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Yes|Yes|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Yes|Yes|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|No|Yes|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|No|Yes|
|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|No|Yes|
|Google Organization Project \[cmdb\_ci\_gcp\_project\]|Yes|Yes|
|Image \[cmdb\_ci\_os\_template\]|No|Yes|
|IP Address \[cmdb\_ci\_ip\_address\]|Yes|Yes|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Yes|Yes|
|Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]|Yes|Yes|
|Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]|Yes|Yes|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Yes|Yes|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Yes|Yes|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Yes|Yes|
|Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]|Yes|Yes|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Yes|Yes|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Yes|Yes|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Yes|Yes|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|No|Yes|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Yes|Yes|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Yes|Yes|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Yes|Yes|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Yes|Yes|

**Note:** Labels are not supported by Google Cloud for the following CI classes:

-   Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]
-   Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]
-   Cloud Network \[cmdb\_ci\_network\]
-   Cloud Organizations \[cmdb\_ci\_cloud\_org\]
-   Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]
-   Compute Security Group \[cmdb\_ci\_compute\_security\_group\]
-   Google Organization Folder \[cmdb\_ci\_gcp\_folder\]
-   Image \[cmdb\_ci\_os\_template\]
-   Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

## Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

The following attributes in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Cluster Resource ID|cluster\_resource\_id|
|IP Address|ip\_address|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Port|port|
|Cluster Version|cluster\_version|
|Description|short\_description|
|Install Status|install\_status|
|Operational status|operational\_status|
|SelfLink|self\_link|
|Subnet Mask|subnet\_mask|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Cluster of::Cluster|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]

The following attributes in the Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Comments|comments|
|Description|short\_description|
|Install Status|install\_status|
|Operational status|operational\_status|
|Kubernetes Cluster|cluster|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|
|Kubernetes Cluster Role \[cmdb\_ci\_kubernetes\_cluster\_role\]|Reference|Key Value \[cmdb\_key\_value\]|

## Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]

The following attributes in the Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Comments|comments|
|Description|short\_description|
|Install Status|install\_status|
|Name|name|
|Kubernetes Cluster|cluster|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|
|Kubernetes Cluster Role Binding \[cmdb\_ci\_kubernetes\_cluster\_role\_binding\]|Reference|Key Value \[cmdb\_key\_value\]|

## Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

The following attributes in the Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Available Replicas|available\_replicas|
|Description|short\_description|
|Desired Replicas|desired\_replicas|
|Install Status|install\_status|
|Kubernetes Cluster|cluster|
|Operational status|operational\_status|
|Total Replicas|total\_replicas|
|Unavailable Replicas|unavailable\_replicas|
|Updated Replicas|updated\_replicas|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

The following attributes in the Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Description|short\_description|
|Install Status|install\_status|
|Namespace|namespace|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

The following attributes in the Kubernetes Node \[cmdb\_ci\_kubernetes\_node\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Description|short\_description|
|Install Status|install\_status|
|Namespace|namespace|
|Operational status|operational\_status|
|Kubernetes Cluster|cluster|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Reference|Key Value \[cmdb\_key\_value\]|

## Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]

The following attributes in the Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Disk Type|disk\_type|
|Image Type|image\_type|
|Install Status|install\_status|
|Machine Type|machine\_type|
|Operational status|operational\_status|
|Pod CIDR Range|podIpv4CidrSize|
|Resource version|resource\_version|
|Kubernetes Cluster|cluster|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]|Uses::Used by|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

The following attributes in the Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Description|short\_description|
|Host IP|host\_ip|
|Install Status|install\_status|
|IP Address|ip\_address|
|Operational status|operational\_status|
|Resource version|resource\_version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Container \[cmdb\_ci\_docker\_container\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]

The following attributes in the Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Description|short\_description|
|Desired Replicas|desired\_replicas|
|Install Status|install\_status|
|Operational status|operational\_status|
|SelfLink|self\_link|
|Total Replicas|total\_replicas|
|Kubernetes Cluster|cluster|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

The following attributes in the Kubernetes Service \[cmdb\_ci\_kubernetes\_service\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Description|short\_description|
|Install Status|install\_status|
|IP Address|ip\_address|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

The following attributes in the Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Mount Path|mount\_path|
|Name|name|
|Volume ID|volume\_id|
|Namespace|namespace|

## Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

The following attributes in the Load Balancer Pool \[cmdb\_ci\_lb\_pool\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Reference|Key Value \[cmdb\_key\_value\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]

The following attributes in the Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Load Balancer Service \[cmdb\_ci\_lb\_service\]

The following attributes in the Load Balancer Service \[cmdb\_ci\_lb\_service\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Name|name|
|Object ID|object\_id|
|Port|port|
|Install Status|install\_status|
|Listener Protocol|listener\_protocol|
|Operational status|operational\_status|
|Service Type|service\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Contains::Contained by|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Reference|Key Value \[cmdb\_key\_value\]|

## Network ACL \[cmdb\_ci\_network\_acl\]

The following attributes in the Network ACL \[cmdb\_ci\_network\_acl\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Description|short\_description|
|Install Status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network ACL \[cmdb\_ci\_network\_acl\]|Contains::Contained by|Network ACL Rule \[cmdb\_ci\_network\_acl\_rule\]|
|Network ACL \[cmdb\_ci\_network\_acl\]|Reference|Key Value \[cmdb\_key\_value\]|

## Network ACL Rule \[cmdb\_ci\_network\_acl\_rule\]

The following attributes in the Network ACL Rule \[cmdb\_ci\_network\_acl\_rule\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Allow Deny|allow\_deny|
|Allowed\\Denied Traffic|allowed\_denied\_traffic|
|Destination Ranges|destination\_ranges|
|Install Status|install\_status|
|Operational status|operational\_status|
|Outbound|is\_outbound|
|Source Ranges|source\_ranges|
|Target Tags|target\_tags|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network ACL Rule \[cmdb\_ci\_network\_acl\_rule\]|Reference|Key Value \[cmdb\_key\_value\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Class|sys\_class\_name|
|CPU count|cpu\_count|
|Disk space \(GB\)|disk\_space|
|Host name|host\_name|
|Install Status|install\_status|
|IP Address|ip\_address|
|Is Virtual|virtual|
|Operating System|os|
|Operational status|operational\_status|
|OS Version|os\_version|
|RAM \(MB\)|ram|

**Note:** If the GCP Systems Manager \(SSM\) service isn't enabled, the connector populates the server records in the Server \[cmdb\_ci\_server\] class. If the GCP SSM service is enabled, then based on the platform type obtained through the SSM service, the server records are populated in either the Linux Server \[cmdb\_ci\_linux\_server\] class or the Windows Server \[cmdb\_ci\_win\_server\] class. The Server \[cmdb\_ci\_server\] class is the parent class of the Linux Server \[cmdb\_ci\_linux\_server\] and the Windows Server \[cmdb\_ci\_win\_server\] classes.

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Server \[cmdb\_ci\_server\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|
|Server \[cmdb\_ci\_server\]|Reference|Key Value \[cmdb\_key\_value\]|
|Server \[cmdb\_ci\_server\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]

The following attributes in the SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Resource ID|resource\_id|
|Folder ID|folder\_id|
|Organization ID|organization\_id|
|Parent|parent|
|Project|project|
|Project ID|project\_id|
|Self Link|self\_link|
|Service Graph Connection Record|sg\_connection\_record|
|Region|region|
|Resource Type|resource\_type|
|Organization-Credential Record|org\_credential\_record|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data when the Software Asset Management \(SAM\) application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Discovery source|discovery\_source|
|Name|name|
|Version|version|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data when the SAM application is installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Display name|display\_name|
|Publisher|publisher|
|Version|version|
|Discovery source|discovery\_source|
|Last scanned|last\_scanned|
|Installed on|installed\_on|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Installation \[cmdb\_sam\_sw\_install\]|Reference|Server \[cmdb\_ci\_server\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data when the SAM application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Installed on|installed\_on|
|Install date|install\_date|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Server \[cmdb\_ci\_server\]|

## Storage Mapping \[cmdb\_ci\_storage\_mapping\]

The following attributes in the Storage Mapping \[cmdb\_ci\_storage\_mapping\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Mapping Type|mapping\_type|
|Operational status|operational\_status|

## Storage Volume \[cmdb\_ci\_storage\_volume\]

The following attributes in the Storage Volume \[cmdb\_ci\_storage\_volume\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Volume ID|volume\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Size bytes|size\_bytes|
|State|state|
|Storage type|storage\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Reference|Key Value \[cmdb\_key\_value\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]

The following attributes in the Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Capacity|capacity|
|Install Status|install\_status|
|Operational status|operational\_status|
|Parent ID|parent\_id|
|Size \(GB\)|size|
|State|state|
|Volume Name|volume\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Provisioned From::Provisioned|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Reference|Key Value \[cmdb\_key\_value\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|CPUs|cpus|
|Disks|disks|
|Disks size \(GB\)|disks\_size|
|Install Status|install\_status|
|IP Address|ip\_address|
|Memory \(MB\)|memory|
|Network adapters|nics|
|Operational status|operational\_status|
|State|state|
|Termination Protection|termination\_protection|
|VM Instance ID|vm\_inst\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|Storage Mapping \[cmdb\_ci\_storage\_mapping\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Google Organization Project \[cmdb\_ci\_gcp\_project\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|Key Value \[cmdb\_key\_value\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\]|

## VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]

The following attributes in the VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|IP Address|ip\_address|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|

## Related content

[Data mapping for Service Graph Connector for GCP](cmdb-data-mapping-gcp.md)

[Service Graph Connector for GCP properties](cmdb-sgc-gcp-props.md)

