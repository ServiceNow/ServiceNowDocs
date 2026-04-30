---
title: Target tables for storing Service Graph Connector for Wiz data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from a Wiz project. The data is saved in tables that extend from the CMDB CI classes and other non-CMDB classes.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-11-03"
reading_time_minutes: 19
breadcrumb: [Wiz, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing Service Graph Connector for Wiz data

When you complete setting up the connection, you can configure the integration to periodically pull data from a Wiz project. The data is saved in tables that extend from the CMDB CI classes and other non-CMDB classes.

## AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

The following attributes in the AWS Datacenter \[cmdb\_ci\_aws\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Region|region|externalId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

The following attributes in the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Region|region|externalId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Resource Group \[cmdb\_ci\_resource\_group\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Cloud DataBase \[cmdb\_ci\_cloud\_database\]

The following attributes in the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|
|Type|type|nativeType|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]

The following attributes in the Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Cluster ID|cluster\_id|externalId|
|Name|name|name|
|Cluster Type|cluster\_type|kind|
|Install Status|install\_status|None|
|Vendor|vendor|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud DataBase Cluster \[cmdb\_ci\_cloud\_db\_cluster\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Cloud Disk Type \[cmdb\_ci\_disk\_type\]

The following attributes in the Cloud Disk Type \[cmdb\_ci\_disk\_type\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|properties.volumeType, zone|
|Object ID|object\_id|properties.volumeType, zone|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Disk Type \[cmdb\_ci\_disk\_type\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|

## Cloud Function \[cmdb\_ci\_cloud\_function\]

The following attributes in the Cloud Function \[cmdb\_ci\_cloud\_function\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|CodeSha256|codesha256|awsLambda\_codeSha256|
|Install Status|install\_status|None|
|Language|language|runtime|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]

The following attributes in the Cloud Gateway \[cmdb\_ci\_cloud\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]

The following attributes in the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Provider|provider|cloudPlatform|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|

## Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

The following attributes in the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table are populated by collected data:

<table id="table_edq_2mb_f1c"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Wiz attribute

</th></tr></thead><tbody><tr><td>

Name

</td><td>

name

</td><td>

name

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td><td>

name \(for AWS Load Balancer v1\)externalId \(for Azure and AWS Load Balancer v2\)

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

None

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

The following attributes in the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|MAC Address|mac\_address|macAddress|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Cloud Network \[cmdb\_ci\_network\]

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Cidr|cidr|addressRanges|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Network \[cmdb\_ci\_network\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Network \[cmdb\_ci\_network\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

The following attributes in the Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\] table are populated by collected data:

<table id="table_hzl_5nb_f1c"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Wiz attribute

</th></tr></thead><tbody><tr><td>

Name

</td><td>

name

</td><td>

name

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td><td>

externalId \(for Azure and GCP\)providerUniqueId \(for AWS\)

</td></tr><tr><td>

Cloud Provider

</td><td>

cloud\_provider

</td><td>

cloudPlatform

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

None

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Organizations \[cmdb\_ci\_cloud\_org\]

The following attributes in the Cloud Organizations \[cmdb\_ci\_cloud\_org\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Object ID|object\_id|ProviderUniqueId\(AWS and Azure\), externalId \(for GCP\)|
|Name|name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]

The following attributes in the Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\] table are populated by collected data:

<table id="table_drz_h3s_g1c"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Wiz attribute

</th></tr></thead><tbody><tr><td>

Name

</td><td>

name

</td><td>

name

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td><td>

externalId \(for Azure and GCP\)ProviderUniqueId \(for AWS\)

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

None

</td></tr><tr><td>

Public IP Address

</td><td>

public\_ip\_address

</td><td>

address

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Account Id|account\_id|externalId|
|Name|name|name|
|Object ID|object\_id|externalId|
|Datacenter Type|datacenter\_type|cloudPlatform|
|Is management account|is\_master\_account|ProviderUniqueID \(AWS only\)|
|Organization Id|organization\_id|ProviderUniqueID \(AWS only\)|
|Parent account|parent\_account|ProviderUniqueID \(AWS only\)|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]

The following attributes in the Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Reference|Key Value \[cmdb\_key\_value\]|
|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

The following attributes in the Compute Security Group \[cmdb\_ci\_compute\_security\_group\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|
|Region|region|region|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Reference|Key Value \[cmdb\_key\_value\]|

## Docker Container \[cmdb\_ci\_docker\_container\]

The following attributes in the Docker Container \[cmdb\_ci\_docker\_container\] table are populated by collected data:

<table id="table_jrd_khj_dxb"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Wiz attribute

</th></tr></thead><tbody><tr><td>

Container id

</td><td>

container\_id

</td><td>

externalId \(for Kubernetes, ACA, and ACI\)providerUniqueId \(for ECS\)

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

None

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

name

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Docker Container \[cmdb\_ci\_docker\_container\]|Hosts:: Hosted on|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\] \(for ECS\)|
|Docker Container \[cmdb\_ci\_docker\_container\]|Hosts:: Hosted on|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] \(for ACA, ACI\)|
|Docker Container \[cmdb\_ci\_docker\_container\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]

The following attributes in the DynamoDB Table \[cmdb\_ci\_dynamodb\_table\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Reference|Key Value \[cmdb\_key\_value\]|

## Google Datacenter \[cmdb\_ci\_google\_datacenter\]

The following attributes in the Google Datacenter \[cmdb\_ci\_google\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Region|region|externalId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Google Organization Folder \[cmdb\_ci\_gcp\_folder\]

The following attributes in the Google Organization Folder \[cmdb\_ci\_gcp\_folder\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Object ID|object\_id|externalId|
|Name|name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Google Organization Project \[cmdb\_ci\_gcp\_project\]

The following attributes in the Google Organization Project \[cmdb\_ci\_gcp\_project\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Project Id|project\_id|providerUniqueId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Organization Project \[cmdb\_ci\_gcp\_project\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Hardware Type \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|instanceType|
|Object ID|object\_id|instanceType|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|

## Image \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Image \[cmdb\_ci\_os\_template\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Image \[cmdb\_ci\_os\_template\]|Reference|Key Value \[cmdb\_key\_value\]|

**Note:** Data with no subscription IDs for images aren't imported. Also, if the subscription ID for an image is available, but the subscription-specific details are not available in Wiz, the data isn't imported by the connector.

## Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

The following attributes in the Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Install Status|install\_status|None|
|Object ID|object\_id|externalId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|Reference|Key Value \[cmdb\_key\_value\]|

## Internet Gateway \[cmdb\_ci\_internet\_gateway\]

The following attributes in the Internet Gateway \[cmdb\_ci\_internet\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Internet Gateway \[cmdb\_ci\_internet\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Internet Gateway \[cmdb\_ci\_internet\_gateway\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Internet Gateway \[cmdb\_ci\_internet\_gateway\]|Reference|Key Value \[cmdb\_key\_value\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Key|key|tags|
|Value|value|tags|

**Note:** The cloud resource tags \(key-value pairs\) from the API response are populated in the Key Value \[cmdb\_key\_value\] table.

## Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

The following attributes in the Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Cluster Resource ID|cluster\_resource\_id|providerUniqueId|
|Kubernetes UID|k8s\_uid|externalId|
|Name|name|name|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Docker Container \[cmdb\_ci\_docker\_container\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Cluster of::Cluster|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]

The following attributes in the Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\] table are populated by collected data:

<table id="table_cqt_5lc_dxb"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Wiz attribute

</th></tr></thead><tbody><tr><td>

Kubernetes UID

</td><td>

k8s\_uid

</td><td>

uid

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

name

</td></tr><tr><td>

Namespace

</td><td>

namespace

</td><td>

namespace

</td></tr><tr><td>

Available Replicas

</td><td>

available\_replicas

</td><td>

status\_availableReplicas

</td></tr><tr><td>

Desired Replicas

</td><td>

desired\_replicas

</td><td>

spec\_replicas

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

None

</td></tr><tr><td>

Total Replicas

</td><td>

total\_replicas

</td><td>

status\_replicas

</td></tr><tr><td>

Updated Replicas

</td><td>

updated\_replicas

</td><td>

status\_updatedReplicas

</td></tr><tr><td>

Kubernetes Cluster

</td><td>

cluster

</td><td>

Kubernetes\_clusterExternalID

</td></tr><tr><td>

SelfLink

</td><td>

self\_link

</td><td>

api\_versionnamespace

name

</td></tr><tr><td>

Unavailable Replicas

</td><td>

unavailable\_replicas

</td><td>

status\_unavailableReplicas

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]

The following attributes in the Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Install Status|install\_status|None|
|Namespace|namespace|name|
|Kubernetes Cluster|cluster|Kubernetes\_clusterExternalID|
|Name|name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]

The following attributes in the Kubernetes Node \[cmdb\_ci\_kubernetes\_node\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|IP Address|ip\_address|status\_address|
|Kubernetes UID|k8s\_uid|uid|
|Name|name|name|
|Install Status|install\_status|None|
|Kubernetes Cluster|cluster|Kubernetes\_clusterExternalID|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

The following attributes in the Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Kubernetes UID|k8s\_uid|uid|
|Namespace|namespace|namespace|
|Host IP|host\_ip|status\_hostIP|
|Install Status|install\_status|None|
|IP Address|ip\_address|status\_podIPs|
|Kubernetes Cluster|cluster|Kubernetes\_clusterExternalID|
|Name|name|name|
|Resource version|resource\_version|resourceVersion|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]

The following attributes in the Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\] table are populated by collected data:

<table id="table_e53_wgj_dxb"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Wiz attribute

</th></tr></thead><tbody><tr><td>

Kubernetes UID

</td><td>

k8s\_uid

</td><td>

uid

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

name

</td></tr><tr><td>

Namespace

</td><td>

namespace

</td><td>

namespace

</td></tr><tr><td>

Available Replicas

</td><td>

available\_replicas

</td><td>

status\_availableReplicas

</td></tr><tr><td>

Desired Replicas

</td><td>

desired\_replicas

</td><td>

spec\_replicas

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

None

</td></tr><tr><td>

SelfLink

</td><td>

self\_link

</td><td>

api\_versionnamespace

name

</td></tr><tr><td>

Total Replicas

</td><td>

total\_replicas

</td><td>

status\_replicas

</td></tr><tr><td>

Kubernetes Cluster

</td><td>

cluster

</td><td>

Kubernetes\_clusterExternalID

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]

The following attributes in the Kubernetes Service \[cmdb\_ci\_kubernetes\_service\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Kubernetes UID|k8s\_uid|uid|
|Name|name|name|
|Install Status|install\_status|None|
|Kubernetes Cluster|cluster|Kubernetes\_clusterExternalID|
|Namespace|namespace|namespace|
|IP Address|ip\_address|spec\_clusterIP|
|Selector|selector|spec\_selector|
|Service Type|service\_type|spec\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Reference|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Linux Server \[cmdb\_ci\_linux\_server\]

The following attributes in the Linux Server \[cmdb\_ci\_linux\_server\] table are populated by collected data.

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Serial number|serial\_number|providerUniqueId|
|CPU count|cpu\_count|vCPUs|
|Install Status|install\_status|None|
|Is Virtual|None|None|
|Operating System|os|operatingSystem|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Linux Server \[cmdb\_ci\_linux\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]

The following attributes in the Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Region|region|externalId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]

The following attributes in the OCI Datacenter \[cmdb\_ci\_oci\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Region|region|externalId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Resource Group \[cmdb\_ci\_resource\_group\]

The following attributes in the Resource Group \[cmdb\_ci\_resource\_group\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Reference|Key Value \[cmdb\_key\_value\]|

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data:

|Attribute label|Attribute name|Wiz|
|---------------|--------------|---|
|Serial Number|providerUniqueID|providerUniqueId|
|Serial Number Type|serial\_number\_type|None|
|Valid|serial\_number\_valid|providerUniqueId|

**Note:** The Serial Number \[cmdb\_serial\_number\] table is populated for Azure only.

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Server \[cmdb\_ci\_server\]|
|Serial Number \[cmdb\_serial\_number\]|Reference|Windows Server \[cmdb\_ci\_win\_server\]|
|Serial Number \[cmdb\_serial\_number\]|Reference|Linux Server \[cmdb\_ci\_linux\_server\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Serial number|serial\_number|providerUniqueId|
|CPU count|cpu\_count|vCPUs|
|Install Status|install\_status|None|
|Is Virtual|virtual|None|
|Operating System|os|operatingSystem|
|Sys ID|sys\_id|Not applicable|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]

The following attributes in the SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Project ID|project\_id|productIDs|
|CMDB Class|u\_cmdb\_class|None|

**Note:** Cloud resource project IDs are populated in the SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\] table.

## Storage Volume \[cmdb\_ci\_storage\_volume\]

The following attributes in the Storage Volume \[cmdb\_ci\_storage\_volume\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Object ID|object\_id|externalId|
|Volume ID|volume\_id|externalId|
|Install Status|install\_status|None|
|Name|name|name|
|Size|size|sizeGb|
|Size bytes|size\_bytes|sizeGb|
|Storage type|storage\_type|volumeType|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Reference|Key Value \[cmdb\_key\_value\]|

## Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]

The following attributes in the Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\] table is populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Object ID|object\_id|externalId|
|Name|name|name|
|Install Status|install\_status|None|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Reference|Key Value \[cmdb\_key\_value\]|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data:

<table id="table_ihz_r2j_dxb"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th><th>

Wiz attribute

</th></tr></thead><tbody><tr><td>

Name

</td><td>

name

</td><td>

name

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td><td>

externalId

</td></tr><tr><td>

CPUs

</td><td>

cpus

</td><td>

vCPUs

</td></tr><tr><td>

Disks

</td><td>

disks

</td><td>

totalDisks

</td></tr><tr><td>

Install Status

</td><td>

install\_status

</td><td>

None

</td></tr><tr><td>

Memory \(MB\)

</td><td>

memory

</td><td>

memoryGB

</td></tr><tr><td>

VM Instance ID

</td><td>

vm\_inst\_id

</td><td>

externalIdproviderUniqueId \(for Azure\)

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|OCI Datacenter \[cmdb\_ci\_oci\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Managed by::Manages|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|
|Windows Server \[cmdb\_ci\_win\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Linux Server \[cmdb\_ci\_linux\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Server \[cmdb\_ci\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Reference|Key Value \[cmdb\_key\_value\]|

## VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]

The following attributes in the VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|externalId|
|Object ID|object\_id|externalId|
|Region|region|externalId|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|VMware vCenter Datacenter \[cmdb\_ci\_vcenter\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Windows Server \[cmdb\_ci\_win\_server\]

The following attributes in the Windows Server \[cmdb\_ci\_win\_server\] table are populated by collected data.

|Attribute label|Attribute name|Wiz attribute|
|---------------|--------------|-------------|
|Name|name|name|
|Object ID|object\_id|externalId|
|Serial number|providerUniqueID|providerUniqueId|
|CPU count|cpu\_count|vCPUs|
|Install Status|install\_status|None|
|Is Virtual|None|None|
|Operating System|os|operatingSystem|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Windows Server \[cmdb\_ci\_win\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

