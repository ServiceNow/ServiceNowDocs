---
title: CMDB classes targeted in Service Graph Connector for AWS
description: When you complete setting up the connection, you can configure the integration to periodically pull data from AWS. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 17
breadcrumb: [AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for AWS

When you complete setting up the connection, you can configure the integration to periodically pull data from AWS. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Amazon Redshift \[cmdb\_ci\_aws\_redshift\]

The following attributes in the Amazon Redshift \[cmdb\_ci\_aws\_redshift\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|TCP port\(s\)|tcp\_port|
|Cluster Availability Status|cluster\_availability\_status|
|Install Status|install\_status|
|Availability Zone|availability\_zone|
|Fully qualified domain name|fqdn|
|Node Count|node\_count|
|Node Type|node\_type|
|Operational status|operational\_status|
|Start date|start\_date|
|VPC ID|vpc\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Amazon Redshift \[cmdb\_ci\_aws\_redshift\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Amazon Redshift \[cmdb\_ci\_aws\_redshift\]|Reference|Availability Zone \[cmdb\_ci\_availability\_zone\]|

## Application \[cmdb\_ci\_appl\]

The following attributes in the Application \[cmdb\_ci\_appl\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Version|version|
|TCP port\(s\)|tcp\_port|
|Running Process|running\_process|
|Running process key parameters|running\_process\_key\_parameters|
|Name|name|
|Running process command|running\_process\_command|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Server \[cmdb\_ci\_server\]|

## Availability Zone \[cmdb\_ci\_availability\_zone\]

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

## AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

The following attributes in the AWS Datacenter \[cmdb\_ci\_aws\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Region|region|
|Install Status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availablity\_zone\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]

The following attributes in the AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Org Unit Parent ID|org\_unit\_parent\_id|
|Organizational ID|aws\_org\_id|
|Root ID|root\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|Contains::Contained by|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Block Endpoint \[cmdb\_ci\_endpoint\_block\]

The following attributes in the Block Endpoint \[cmdb\_ci\_endpoint\_block\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|

## Cloud DataBase \[cmdb\_ci\_cloud\_database\]

The following attributes in the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|TCP port\(s\)|tcp\_port|
|Automated Backups|automated\_backup|
|Category|category|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|
|Type|type|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Function \[cmdb\_ci\_cloud\_function\]

The following attributes in the Cloud Function \[cmdb\_ci\_cloud\_function\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Code Size|code\_size|
|CodeSha256|codesha256|
|Function Last Modified|function\_last\_modified|
|Install Status|install\_status|
|Language|language|
|Operational status|operational\_status|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]

The following attributes in the Cloud Gateway \[cmdb\_ci\_cloud\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]

The following attributes in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Provider|provider|
|Cores|cores|
|Install Status|install\_status|
|IP Address|ip\_address|
|Local Storage GB|local\_storage\_gb|
|Memory MB|memory\_mb|
|Operational status|operational\_status|
|vCPUs|vcpus|
|Zone|zone|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Cloud Image \[cmdb\_ci\_cloud\_os\_image\]

The following attributes in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Description|short\_description|
|Environment|environment|
|Guest OS|guest\_os|
|Image Source|image\_source|
|Image Type|image\_type|
|Provider|provider|
|Root Device Type|root\_device\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Reference|Key Value|

## Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

The following attributes in the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Canonical Hosted Zone ID|canonical\_hosted\_zone\_id|
|Canonical Hosted Zone Name|canonical\_hosted\_zone\_name|
|DNS Name|dns\_name|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|Key Value \[cmdb\_key\_value\]|

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
|Private DNS|private\_dns|
|Private IP|private\_ip|
|Public DNS|public\_dns|
|State|state|
|Configuration Item|cmdb\_ci|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Reference|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Cloud Network \[cmdb\_ci\_network\]

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Cidr|cidr|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
|Cloud Network \[cmdb\_ci\_network\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

The following attributes in the Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|ACL Access Type|acl\_access\_type|
|Cloud Provider|cloud\_provider|
|Creation Date|creation\_date|
|Encryption Type|encryption\_type|
|Install Status|install\_status|
|Operational status|operational\_status|
|Policy Access Type|policy\_access\_type|
|Service Name|service\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Organizations \[cmdb\_ci\_cloud\_org\]

The following attributes in the Cloud Organizations \[cmdb\_ci\_cloud\_org\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Install Status|install\_status|
|Master Email|master\_email|
|Name|name|
|Operational status|operational\_status|
|Root ID|root\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|

## Cloud Resource \[cmdb\_ci\_cmp\_resource\]

The following attributes in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Description|short\_description|
|Install Status|install\_status|
|Operational status|operational\_status|
|Resource type|resource\_type|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Account Email|account\_email|
|Install Status|install\_status|
|Is management account|is\_master\_account|
|Operational status|operational\_status|
|Parent account|parent\_account|
|Datacenter Type|datacenter\_type|
|Account Id|account\_id|
|Object ID|object\_id|
|Organization Id|organization\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

The following attributes in the Cloud Subnet \[cmdb\_ci\_cloud\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Available IP Count|available\_ip\_count|
|CIDR|cidr|
|Install Status|install\_status|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Reference|Key Value \[cmdb\_key\_value\]|

## Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

The following attributes in the Compute Security Group \[cmdb\_ci\_compute\_security\_group\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Reference|Key Value \[cmdb\_key\_value\]|

## Docker Container \[cmdb\_ci\_docker\_container\]

The following attributes in the Docker Container \[cmdb\_ci\_docker\_container\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Container id|container\_id|
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
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Docker Image \[cmdb\_ci\_docker\_image\]|Instantiates::Instantiated by|Docker Container \[cmdb\_ci\_docker\_container\]|

## DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]

The following attributes in the DynamoDB Table \[cmdb\_ci\_dynamodb\_table\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Cloud Provider|cloud\_provider|
|Creation Date|creation\_date|
|Encryption|encryption|
|Install Status|install\_status|
|Operational status|operational\_status|
|Read Units|read\_units|
|Service Name|service\_name|
|Write Units|write\_units|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Reference|Key Value \[cmdb\_key\_value\]|

## Hardware Type \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Cores|cores|
|Install Status|install\_status|
|Local Storage GB|local\_storage\_gb|
|Memory MB|memory\_mb|
|Operational status|operational\_status|
|vCPUs|vcpus|

**Note:** If the **sn\_itom\_pattern.use a single hardware type for cloud data center** property is set to `true`, hardware type data is populated in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table. If this property is set to `false`, hardware type data is populated in the Hardware Type \[cmdb\_ci\_compute\_template\] table. Before you configure the **sn\_itom\_pattern.use a single hardware type for cloud data center** property, the existing hardware type data must be cleaned. For instructions, see the [Service Graph Connector For AWS - Migrating to a new hardware type model \[KB1705233\]](https://support.servicenow.com/kb?sys_kb_id=c5700bf647dd9250f64de825126d43b0&id=kb_article_view) article in the Now Support Knowledge Base.

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Image \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Class|sys\_class\_name|
|Description|short\_description|
|Environment|environment|
|Guest OS|guest\_os|
|Image Source|image\_source|
|Image Type|image\_type|
|Install Status|install\_status|
|Operational status|operational\_status|
|Root Device Type|root\_device\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Image \[cmdb\_ci\_os\_template\]|Reference|Key Value|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Nic|nic|
|IP Address|ip\_address|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|Value|

## Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

The following attributes in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Cluster Resource ID|cluster\_resource\_id|
|IP Address|ip\_address|
|Name|name|
|Port|port|
|Fully qualified domain name|fqdn|
|Install status|install\_status|
|Namespace|namespace|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Cluster of::Cluster|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Managed by::Manages|Server \[cmdb\_ci\_server\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Reference|Key Value \[cmdb\_key\_value\]|

## Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]

The following attributes in the Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|
|Operational status|operational\_status|
|SelfLink|self\_link|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

The following attributes in the Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Available Replicas|available\_replicas|
|Install Status|install\_status|
|Operational status|operational\_status|
|SelfLink|self\_link|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

The following attributes in the Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Install Status|install\_status|
|Namespace|namespace|
|Operational status|operational\_status|

## Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

The following attributes in the Kubernetes Node \[cmdb\_ci\_kubernetes\_node\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Install Status|install\_status|
|Operational status|operational\_status|

## Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

The following attributes in the Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|
|IP Address|ip\_address|
|Operational status|operational\_status|
|Resource version|resource\_version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Container \[cmdb\_ci\_docker\_container\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Image \[cmdb\_ci\_docker\_image\]|

## Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]

The following attributes in the Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|
|Operational status|operational\_status|
|SelfLink|self\_link|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|

## Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

The following attributes in the Kubernetes Service \[cmdb\_ci\_kubernetes\_service\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|
|Install Status|install\_status|
|IP Address|ip\_address|
|Operational status|operational\_status|
|Selector|selector|

## Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]

The following attributes in the Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Kubernetes UID|k8s\_uid|
|Mount Path|mount\_path|
|Name|name|
|Volume ID|volume\_id|
|Install Status|install\_status|
|Namespace|namespace|
|Operational status|operational\_status|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|MAC Address|mac\_address|
|Configuration Item|cmdb\_ci|
|Name|name|
|Install Status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Server \[cmdb\_ci\_server\], Linux Server \[cmdb\_ci\_linux\_server\], or Windows Server \[cmdb\_ci\_win\_server\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

<table id="table_wv4_kvh_k5b"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Data source

</th></tr></thead><tbody><tr><td>

Name

</td><td>

name

</td><td>

SG-AWS-SSM-GetS3Object

 SG-AWS-Get-Inventory \(if the AWS SSM service is enabled\)

 SG-AWS-EC2 \(if the AWS SSM service isn't enabled\)

</td></tr><tr><td>

Class

</td><td>

sys\_class\_name

</td><td>

SG-AWS-Software-Inventory \(if the AWS SSM service is enabled\)

</td></tr><tr><td>

CPU core count

</td><td>

cpu\_core\_count

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

CPU core thread

</td><td>

cpu\_core\_thread

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

CPU count

</td><td>

cpu\_count

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

CPU name

</td><td>

cpu\_name

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

CPU manufacturer

</td><td>

cpu\_manufacturer

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

CPU speed \(MHz\)

</td><td>

cpu\_speed

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

CPU type

</td><td>

cpu\_type

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

Disk Space \(GB\)

</td><td>

disk\_space

</td><td>

SG-AWS-SSM-GetS3Object

 SG-AWS-EC2

</td></tr><tr><td>

DNS Domain

</td><td>

dns\_domain

</td><td>

SG-AWS-EC2

</td></tr><tr><td>

Fully qualified domain name

</td><td>

fqdn

</td><td>

SG-AWS-EC2

</td></tr><tr><td>

Host Name

</td><td>

host\_name

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

SG-AWS-EC2

</td></tr><tr><td>

Is Virtual

</td><td>

virtual

</td><td>

SG-AWS-EC2

</td></tr><tr><td>

Model ID

</td><td>

model\_id

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td><td>

SG-AWS-EC2

</td></tr><tr><td>

Operating System

</td><td>

os

</td><td>

SG-AWS-EC2

 SG-AWS-Software-Inventory

</td></tr><tr><td>

Operational status

</td><td>

operational\_status

</td><td>

SG-AWS-EC2

</td></tr><tr><td>

OS Version

</td><td>

os\_version

</td><td>

SG-AWS-Software-Inventory

</td></tr><tr><td>

RAM \(MB\)

</td><td>

ram

</td><td>

SG-AWS-SSM-GetS3Object

 SG-AWS-EC2

</td></tr><tr><td>

Serial Number

</td><td>

serial\_number

</td><td>

SG-AWS-SSM-GetS3Object

</td></tr></tbody>
</table>**Note:**

-   If the AWS Systems Manager \(SSM\) service isn't enabled, the connector populates the server records in the Server \[cmdb\_ci\_server\] class. If the AWS SSM service is enabled, then based on the platform type obtained through the SSM service, the server records are populated in either the Linux Server \[cmdb\_ci\_linux\_server\] class or the Windows Server \[cmdb\_ci\_win\_server\] class. The Server \[cmdb\_ci\_server\] class is the parent class of the Linux Server \[cmdb\_ci\_linux\_server\] and the Windows Server \[cmdb\_ci\_win\_server\] classes.
-   If the AWS SSM service is enabled, the **name** field is populated by the SG-AWS-Get-Inventory data source, and the **sys\_class\_name** field is populated by the SG-AWS-Software-Inventory data source. If the AWS SSM service isn't enabled, the **name** field is populated by the SG-AWS-EC2 data source, and the **sys\_class\_name** field isn't populated.

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Server \[cmdb\_ci\_server\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|
|Server \[cmdb\_ci\_server\]|Reference|Key Value \[cmdb\_key\_value\]|

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
|Host|host|
|Install Status|install\_status|
|Mapping Type|mapping\_type|
|Mount Point|mount\_point|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Mapping \[cmdb\_ci\_storage\_mapping\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|

## Storage Volume \[cmdb\_ci\_storage\_volume\]

The following attributes in the Storage Volume \[cmdb\_ci\_storage\_volume\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Volume ID|volume\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Size|size|
|Size bytes|size\_bytes|
|State|state|
|Storage Type|storage\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Reference|Key Value \[cmdb\_key\_value\]|

## Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]

The following attributes in the Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|CPUs|cpus|
|Disks|disks|
|Disks size \(GB\)|disks\_size|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|IP Address|ip\_address|
|Memory \(MB\)|memory|
|Monitor|monitor|
|Network adapters|nics|
|Operational status|operational\_status|
|Placement Group ID|placement\_group\_id|
|State|state|
|VM Instance ID|vm\_inst\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Located in::Houses|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|Storage Mapping \[cmdb\_ci\_storage\_mapping\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|Key Value \[cmdb\_key\_value\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|

## VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]

The following attributes in the VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|

## Related content

[Data mapping for Service Graph Connector for AWS](cmdb-data-mapping-aws.md)

[Service Graph Connector for AWS properties](cmdb-sgc-aws-props.md)

