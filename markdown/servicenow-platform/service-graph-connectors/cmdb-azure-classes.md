---
title: CMDB classes targeted in Service Graph Connector for Microsoft Azure
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Microsoft Azure. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-02"
reading_time_minutes: 12
breadcrumb: [Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Microsoft Azure

When you complete setting up the connection, you can configure the integration to periodically pull data from Microsoft Azure. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

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
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Computer \[cmdb\_ci\_computer\]|

## Availability Zone \[cmdb\_ci\_availability\_zone\]

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Reference|Key Value \[cmdb\_key\_value\]|

## Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

The following attributes in the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Comments|comments|
|Name|name|
|Object ID|object\_id|
|Region|region|
|Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Resource Group \[cmdb\_ci\_resource\_group\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

## Cloud DataBase \[cmdb\_ci\_cloud\_database\]

The following attributes in the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|
|Type|type|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Function \[cmdb\_ci\_cloud\_function\]

The following attributes in the Cloud Function \[cmdb\_ci\_cloud\_function\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|App Function state|app\_function\_state|
|Code Location URL|code\_location\_url|
|Fully qualified domain name|fqdn|
|Function Last Modified|function\_last\_modified|
|Install Status|install\_status|
|IP Address|ip\_address|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

The following attributes in the Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|IP Address|ip\_address|
|IPAddress Type|ipaddress\_type|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|

## Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

The following attributes in the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Canonical Hosted Zone Name|canonical\_hosted\_zone\_name|
|DNS Name|dns\_name|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|IP Address|ip\_address|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

The following attributes in the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration Item|cmdb\_ci|
|Install Status|install\_status|
|IP Address|ip\_address|
|MAC Address|mac\_address|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|Primary|primary|
|Private IP|private\_ip|
|Public DNS|public\_dns|
|Public IP|public\_ip|
|State|state|
|Static|is\_static|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Contains::Contained by|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Reference|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Cloud Network \[cmdb\_ci\_network\]

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Cidr|cidr|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]

The following attributes in the Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|Public DNS|public\_dns|
|Public IP Address|public\_ip\_address|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Resource \[cmdb\_ci\_cmp\_resource\]

The following attributes in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Description|short\_description|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|Resource type|resource\_type|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Name|name|
|Object ID|object\_id|
|Datacenter Type|datacenter\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]

The following attributes in the Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Blob Service|blob\_service|
|File Service|file\_service|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Queue Service|queue\_service|
|Sku Name|sku\_name|
|State|state|
|Table Service|table\_service|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

The following attributes in the Cloud Subnet \[cmdb\_ci\_cloud\_subnet\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|CIDR|cidr|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Reference|Key Value \[cmdb\_key\_value\]|

## Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

The following attributes in the Compute Security Group \[cmdb\_ci\_compute\_security\_group\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Reference|Key Value \[cmdb\_key\_value\]|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|CPU core count|cpu\_core\_count|
|CPU count|cpu\_count|
|Disk space \(GB\)|disk\_space|
|IP Address|ip\_address|
|Is Virtual|virtual|
|Object ID|object\_id|
|Operating System|os|
|Operational status|operational\_status|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Serial number|serial\_number|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

For information about the classification of VDIs into the Computer \[cmdb\_ci\_computer\] CI class, see the [Classification of VDIs into computer class using Service graph connector for Azure \[KB2184443\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2184443) article in the Now Support Knowledge Base.

## Hardware Type \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Class|sys\_class\_name|
|Cores|cores|
|Logical Storage GB|local\_storage\_gb|
|Memory MB|memory\_mb|
|vCPUs|vcpus|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

**Note:** When the Cloud Hardware Type class extension is enabled, the **Class** attribute is set to `Cloud Hardware Type`. Else, the attribute is set to `Hardware Type`.

As a user with the admin role, you can enable the Cloud Hardware Type class extension by setting the **use a single hardware type for cloud data centers** property \(**sn\_itom\_pattern.use a single hardware type for cloud data centers**\) to `true`. For more information, see the [Service Graph Connector For Microsoft Azure - Migrating to a new hardware type model \[KB1288455\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1288455) article in the Now Support Knowledge Base.

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Image \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Guest OS|guest\_os|
|Image Source|image\_source|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Offer|offer|
|Operational status|operational\_status|
|Version|version|
|Vendor|vendor|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

The following attributes in the Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Owned By Configuration Item|owned\_by\_cmdb\_ci|
|IP Address|ip\_address|
|Name|name|
|Nic|nic|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

The following attributes in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Cluster Resource ID|cluster\_resource\_id|
|Cluster Version|cluster\_version|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Name|name|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Linux Server \[cmdb\_ci\_linux\_server\]

The following attributes in the Linux Server \[cmdb\_ci\_linux\_server\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|CPU core count|cpu\_core\_count|
|Disk space \(GB\)|disk\_space|
|Install Status|install\_status|
|Is Virtual|virtual|
|Name|name|
|Object ID|object\_id|
|Operating System|os|
|Operational status|operational\_status|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Serial number|serial\_number|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Linux Server \[cmdb\_ci\_linux\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Resource Group \[cmdb\_ci\_resource\_group\]

The following attributes in the Resource Group \[cmdb\_ci\_resource\_group\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|Install Status|install\_status|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Image \[cmdb\_ci\_os\_template\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Reference|Key Value \[cmdb\_key\_value\]|

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Server \[cmdb\_ci\_server\]|
|Serial Number \[cmdb\_serial\_number\]|Reference|Windows Server \[cmdb\_ci\_win\_server\]|
|Serial Number \[cmdb\_serial\_number\]|Reference|Linux Server \[cmdb\_ci\_linux\_server\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|CPU core count|cpu\_core\_count|
|CPU count|cpu\_count|
|Disk space \(GB\)|disk\_space|
|Install Status|install\_status|
|Is Virtual|virtual|
|Name|name|
|Object ID|object\_id|
|Operating System|os|
|Operational status|operational\_status|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Serial number|serial\_number|
|Comments|comments|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Server \[cmdb\_ci\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

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
|Display name|display\_name|
|Publisher|publisher|
|Version|version|
|Discovery source|discovery\_source|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Storage Volume \[cmdb\_ci\_storage\_volume\]

The following attributes in the Storage Volume \[cmdb\_ci\_storage\_volume\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|Size|size|
|Size bytes|size\_bytes|
|State|state|
|Volume ID|volume\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Reference|Key Value \[cmdb\_key\_value\]|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|CPUs|cpus|
|Disks size \(GB\)|disks\_size|
|Install Status|install\_status|
|IP Address|ip\_address|
|Memory \(MB\)|memory|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|
|State|state|
|VM Instance ID|vm\_inst\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Managed by::Manages|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Contains::Contained by|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Uses:Used by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|Key Value \[cmdb\_key\_value\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Windows Server \[cmdb\_ci\_win\_server\]

The following attributes in the Windows Server \[cmdb\_ci\_win\_server\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|CPU core count|cpu\_core\_count|
|Disk space \(GB\)|disk\_space|
|Install Status|install\_status|
|Is Virtual|virtual|
|Name|name|
|Object ID|object\_id|
|Operating System|os|
|Operational status|operational\_status|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Serial number|serial\_number|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Windows Server \[cmdb\_ci\_win\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Related content

[Data mapping for Service Graph Connector for Microsoft Azure](cmdb-data-mapping-azure.md)

[Service Graph Connector for Microsoft Azure properties](cmdb-sgc-azure-props.md)

