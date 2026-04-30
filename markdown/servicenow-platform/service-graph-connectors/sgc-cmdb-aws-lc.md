---
title: Life cycle management of records in Service Graph Connector for AWS
description: Life cycle management in the Service Graph Connector for AWS monitors and updates the statuses of AWS resources throughout their entire life cycle, from creation to deletion.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle management of records in Service Graph Connector for AWS

Life cycle management in the Service Graph Connector for AWS monitors and updates the statuses of AWS resources throughout their entire life cycle, from creation to deletion.

The life cycle management process helps maintain the accuracy and integrity of data in the Configuration Management Database \(CMDB\).

In life cycle management, the record removal process involves systematically deleting obsolete or unnecessary resources. This step ensures that outdated entries are cleared, keeping the CMDB accurate and up-to-date. See [Record removal process in Service Graph Connector for AWS](sgc-cmdb-aws-removal.md).

## Life cycle management for CIs in Service Graph Connector for AWS

The following table lists the configuration items \(CIs\) in CMDB and other non-CMDB tables for which life cycle management is available in Service Graph Connector for AWS.

|Data source|CMDB CI classes|Life cycle management available|
|-----------|---------------|-------------------------------|
|SG-AWS-Organization|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Yes|
|SG-AWS-Org-Units|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|Yes|
|SG-AWS-Service-Account|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Yes|
|SG-AWS-Service-Account-Tags|Key Value \[cmdb\_key\_value\]|No|
|SG-AWS-Org-Unit-Accounts|None|No|
|SG-AWS-Datacenters|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|No|
|SG-AWS-VPC|Network Adapter \[cmdb\_ci\_network\_adapter\]|Yes|
|SG-AWS-Subnets|Availability Zone \[cmdb\_ci\_availability\_zone\]|No|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Yes|
|SG-AWS-Network-Interface|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Yes|
|SG-AWS-Security-Group|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Yes|
|SG-AWS-Storage-Volume|Storage Volume \[cmdb\_ci\_storage\_volume\]|Yes|
|Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]|Yes|
|SG-AWS-Image-Private|Image \[cmdb\_ci\_os\_template\]|Yes|
|SG-AWS-EC2|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Yes|
|Server \[cmdb\_ci\_server\]|Yes|
|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|Yes|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Yes|
|Storage Mapping \[cmdb\_ci\_storage\_mapping\]|Yes|
|Image \[cmdb\_ci\_os\_template\]|Yes|
|IP Address \[cmdb\_ci\_ip\_address\]|Yes|
|SG-AWS-Image-Id|Image \[cmdb\_ci\_os\_template\]|Yes|
|SG-AWS-Hardware-Type|Hardware Type \[cmdb\_ci\_compute\_template\]|Yes|
|SG-AWS-VM-Hw-Consolidation|None|No|
|SG-AWS-ELB-V1|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Yes|
|SG-AWS-ELB-V2|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Yes|
|SG-AWS-RDS|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Yes|
|SG-AWS-S3|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|Yes|
|SG-AWS-DynamoDb|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|Yes|
|SG-AWS-API-Gateway|Cloud Gateway \[cmdb\_ci\_cloud\_gateway\]|Yes|
|SG-AWS-Lambda|Cloud Function \[cmdb\_ci\_cloud\_function\]|Yes|
|SG-AWS-Software-Inventory|Software Installation \[cmdb\_sam\_sw\_install\]|No|
|Software \[cmdb\_ci\_spkg\]|No|
|Software Instance \[cmdb\_software\_instance\]|No|
|SG-AWS-Software-Remove|None|No|
|SG-AWS-SSM-SendCommand|TCP Connections \[cmdb\_tcp\]|No|
|Running \[cmdb\_running\_process\]|No|
|Application \[cmdb\_ci\_appl\]|No|
|SG-AWS-Tags|Key Value \[cmdb\_key\_value\]|No|
|SG-AWS-EKS-Cluster|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Yes|
|SG-AWS-EKS-Cluster-2|None|No|
|SG-AWS-EKS-FULL|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Yes|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Yes|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Yes|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Yes|
|Docker Container \[cmdb\_ci\_docker\_container\]|Yes|
|Kubernetes Volume \[cmdb\_ci\_kubernetes\_volume\]|Yes|
|Kubernetes Deployment \[cmdb\_ci\_kubernetes\_deployment\]|Yes|
|Kubernetes DaemonSet \[cmdb\_ci\_kubernetes\_daemonset\]|Yes|
|Kubernetes ReplicaSet \[cmdb\_ci\_kubernetes\_replicaset\]|Yes|
|SG-AWS-Generic-Resources|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Yes|
|SG-AWS-Redshift-Cluster|Amazon Redshift \[cmdb\_ci\_aws\_redshift\]|Yes|
|SG-AWS-Generic-Tags|Key Value \[cmdb\_key\_value\]|No|
|SG-AWS-Get-Inventory|Server \[cmdb\_ci\_server\]|Yes|

**Parent Topic:**[Service Graph Connector for AWS reference](sgc-cmdb-aws-reference.md)

