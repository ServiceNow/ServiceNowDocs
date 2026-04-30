---
title: CMDB classes targeted in Service Graph Connector for Observability - Dynatrace
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Dynatrace. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-05"
reading_time_minutes: 9
breadcrumb: [Observability-Dynatrace, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Observability - Dynatrace

When you complete setting up the connection, you can configure the integration to periodically pull data from Dynatrace. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Application \[cmdb\_ci\_appl\]

The following attributes in the Application \[cmdb\_ci\_appl\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Configuration file|config\_file|
|Installation directory|install\_directory|
|Name|name|
|Operational status|operational\_status|
|Running process command|running\_process\_command|
|Running process key parameters|running\_process key parameters|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Computer \[cmdb\_ci\_computer\]|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Docker Container \[cmdb\_ci\_docker\_container\]|
|Application \[cmdb\_ci\_appl\]|Reference|Key value \[cmdb\_key\_value\]|

**Note:** Based on the Discovery Process Classifications list, the tables that extend the Application \[cmdb\_ci\_appl\] table are populated by the SGO-Dynatrace Processes \[sn\_dynatrace\_integ\_sg\_dynatrace\_processes\] data source.

## Availability Zone \[cmdb\_ci\_availability\_zone\]

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

## AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

The following attributes in the AWS Datacenter \[cmdb\_ci\_aws\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Region|region|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

## Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

The following attributes in the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Region|region|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Calculated Application Service \[cmdb\_ci\_service\_calculated\]

The following attributes in the Calculated Application Service \[cmdb\_ci\_service\_calculated\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Comments|comments|
|Correlation ID|correlation\_id|
|Hide from dashboard|hide\_from\_dashboard|
|Metadata|metadata|
|Name|name|
|Operational status|operational\_status|
|Service Populator|service\_populator|
|Service Populator Status|populator\_status|
|Service Type|type|

**Note:** The **Comments** attribute includes the following information:

-   Service Type
-   Edition
-   TCP Port

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Depends on::Used by|Configuration Item \[cmdb\_ci\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Runs on::Runs|Computer \[cmdb\_ci\_computer\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Contains::Contained by|Group \[cmdb\_ci\_group\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Reference|Key value \[cmdb\_key\_value\]|

## Cloud DataBase \[cmdb\_ci\_cloud\_database\]

The following attributes in the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|State|state|
|TCP port\(s\)|tcp\_port|
|Type|type|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Function \[cmdb\_ci\_cloud\_function\]

The following attributes in the Cloud Function \[cmdb\_ci\_cloud\_function\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Code Size|code\_size|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Language|language|
|Name|name|
|Object ID|object\_id|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]

The following attributes in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Provider|provider|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

The following attributes in the Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|

## Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

The following attributes in the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

The following attributes in the Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Cloud Provider|cloud\_provider|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Service Name|service\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Resource \[cmdb\_ci\_cmp\_resource\]

The following attributes in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Datacenter Type|datacenter\_type|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|

## Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]

The following attributes in the Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Install Status|install\_status|
|Object ID|object\_id|
|Sku Name|sku\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Reference|Key Value \[cmdb\_key\_value\]|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|CPU core count|cpu\_core\_count|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Is Virtual|virtual|
|Name|name|
|Operating System|os|
|OS Version|os\_version|
|RAM \(MB\)|ram|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Key Value \[cmdb\_key\_value\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

## Docker Container \[cmdb\_ci\_docker\_container\]

The following attributes in the Docker Container \[cmdb\_ci\_docker\_container\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Container id|container\_id|
|Install Status|install\_status|
|Name|name|

**Note:** The **Install Status** value is based on the value of the **properties.containerStatus.state** field in the incoming payload.

-   If the **properties.containerStatus.state** value is `running`, the **Install Status** value is set to `1 (Installed)`.
-   If the **properties.containerStatus.state** value is `terminated` or is empty, or if there are any errors, the **Install Status** value is set to `7 (Retired)`.​
-   For all other **properties.containerStatus.state** values, the **Install Status** value isn't updated.​

​

## Docker Image \[cmdb\_ci\_docker\_image\]

The following attributes in the Docker Image \[cmdb\_ci\_docker\_image\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Image id|image\_id|
|Image digest|image\_digest|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Docker Image \[cmdb\_ci\_docker\_image\]|Instantiates::Instantiated by|Docker Container \[cmdb\_ci\_docker\_container\]|

## DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]

The following attributes in the DynamoDB Table \[cmdb\_ci\_dynamodb\_table\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Install Status|install\_status|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Reference|Key Value \[cmdb\_key\_value\]|

## Group \[cmdb\_ci\_group\]

The following attribute in the Group \[cmdb\_ci\_group\] table is populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Group \[cmdb\_ci\_group\]|Contains::Contained by|Application \[cmdb\_ci\_appl\]|

## Hardware Type \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Image \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

The following attributes in the Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Install Status|install\_status|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Reference|Key Value \[cmdb\_key\_value\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Name|name|

## Key value \[cmdb\_key\_value\]

The following attributes in the Key value \[cmdb\_key\_value\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

The following attributes in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Cluster Resource ID|cluster\_resource\_id|
|Install Status|install\_status|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Cluster of::Cluster|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|

## Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

The following attributes in the Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Kubernetes UID|k8s\_uid|
|Name|name|

## Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

The following attributes in the Kubernetes Node \[cmdb\_ci\_kubernetes\_node\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Kubernetes UID|k8s\_uid|
|Name|name|

## Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

The following attributes in the Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Runs on::Runs|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Container \[cmdb\_ci\_docker\_container\]|

## Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

The following attributes in the Kubernetes Service \[cmdb\_ci\_kubernetes\_service\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Kubernetes UID|k8s\_uid|
|Name|name|
|Namespace|namespace|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Is Virtual|virtual|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Server \[cmdb\_ci\_server\]|Reference|Key Value \[cmdb\_key\_value\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Name|name|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery source|discovery\_source|
|Display name|display\_name|
|Version|version|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|IP Address|ip\_address|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|VM Instance ID|vm\_inst\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|Key Value \[cmdb\_key\_value\]|

