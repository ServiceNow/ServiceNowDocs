---
title: Data mapping for Observability-Dynatrace
description: Data from the Dynatrace data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-data-mapping-dynatrace.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-06-09"
reading_time_minutes: 8
breadcrumb: [Observability-Dynatrace, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Observability-Dynatrace

Data from the Dynatrace data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from Dynatrace.

**Important:** The Service Graph Connector for Observability - Dynatrace supports Dynatrace Classic \(v1/v2 APIs\) and is intended for Dynatrace managed \(self‑hosted\) or legacy SaaS environments. If you're using or upgrading to the latest Dynatrace 3rd-generation SaaS platform, you should use the new Service Graph Connector for Observability - Dynatrace SaaS.

For more information on where data is saved when pulling data from Dynatrace, see [CMDB classes targeted in Service Graph Connector for Observability - Dynatrace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md).

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for Observability-Dynatrace.

<table id="table_uqr_txg_jzb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Description

</th><th>

Staging table

</th><th>

CMDB CI classes

</th><th>

Entities

</th></tr></thead><tbody><tr><td>

SGO-Dynatrace Hosts V2

</td><td>

Ingests host data from Dynatrace.Contains computer data.

</td><td>

SGO-Dynatrace Hosts \[sn\_dynatrace\_integ\_sg\_dynatrace\_hosts\]

</td><td>

[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[IP Address \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Serial Number](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

When the Software Asset Management \(SAM\) application isn't installed:

-   [Software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)
-   [Software Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

When the SAM application is installed: [Software Installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

**Note:** Only the operating system data is stored in the Software Packages, Software Instance, and Software Installation CI classes.

</td><td>

Host

</td></tr><tr><td>

SGO-Dynatrace Processes V2

</td><td>

Ingests process data from Dynatrace.Contains running process data.

</td><td>

SGO-Dynatrace Processes \[sn\_dynatrace\_integ\_sg\_dynatrace\_processes\]

</td><td>

The target table is populated using Application Dependency Mapping \(ADM\). The ADM adapter analyzes the imported data and command-line arguments, identifies the appropriate table based on the conditions included in Discovery Process Classifications list, and inserts the data into the table, which extends the Application \[cmdb\_ci\_appl\] table. To learn about process classification, see Discovery classifiers.

 **Note:** The addition of unclassified processes to the Application \[cmdb\_ci\_appl\] table depends on the value of the **sn\_dynatrace\_integ.createUnmatchedApplicationCIs** system property. For more information, see [Service Graph Connector for Observability - Dynatrace properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-cmdb-dynatrace-props.md).

</td><td>

Process

</td></tr><tr><td>

SGO-Dynatrace Process Groups V2

</td><td>

Ingests process group data from Dynatrace.Contains a group of similar running processes.

</td><td>

SGO-Dynatrace Process Groups \[sn\_dynatrace\_integ\_sg\_dynatrace\_process\_groups\]

</td><td>

[Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Process Group

</td></tr><tr><td>

SGO-Dynatrace Services V2

</td><td>

Ingests service data from Dynatrace.Contains information related to services that are detected via the Dynatrace agent.

Can be filtered using advanced settings properties.

</td><td>

SGO-Dynatrace Services \[sn\_dynatrace\_integ\_sg\_dynatrace\_services\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Service

</td></tr><tr><td>

SGO-Dynatrace Applications V2

</td><td>

Ingests application data from Dynatrace.Contains information related to the applications defined manually.

Applications are parents to services representing a higher level, logical group of services.

</td><td>

SGO-Dynatrace Applications \[sn\_dynatrace\_integ\_sg\_dynatrace\_applications\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Application

</td></tr><tr><td>

SGO-Dynatrace Application Rels V2

</td><td>

Ingests application relationships from Dynatrace.Returns the same data as the SGO-Dynatrace Services data source.

Maps relationships between applications and processes that could have been skipped due to filtered services.

</td><td>

SGO-Dynatrace Application Relationships \[sn\_dynatrace\_integ\_sg\_dynatrace\_application\_relationships\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Service

</td></tr><tr><td>

SGO-Dynatrace AWS Application Network LB

</td><td>

Ingests cloud load balancer data from Dynatrace.Contains information related to AWS application and network load balancer.

</td><td>

SGO-Dynatrace AWS Application Network LB \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_application\_network\_lb\]

</td><td>

[Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AWS Network Load BalancerAWS Application Load Balancer

</td></tr><tr><td>

SGO-Dynatrace AWS Datacenters

</td><td>

Ingests AWS datacenter and availability zone data from Dynatrace.Contains information related to AWS datacenters and availability zones.

</td><td>

SGO-Dynatrace AWS Availability Zone \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_availability\_zone\]

</td><td>

[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Availability Zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AWS Availability Zone

</td></tr><tr><td>

SGO-Dynatrace AWS EC2 Instance

</td><td>

Ingests AWS virtual machine instance data from Dynatrace.Contains information related to virtual machine instances, server details, cloud hardware type, cloud image, and tags.

</td><td>

SGO-Dynatrace AWS EC2 Instance \[sn\_dynatrace\_integ\_sg\_dynatrace\_aws\_ec2\_instance\]

</td><td>

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Cloud Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

EC2 Instance

</td></tr><tr><td>

SGO-Dynatrace AWS Elastic Loadbalancer

</td><td>

Ingests cloud load balancer data from Dynatrace.Contains load balancer details and tags.

</td><td>

SGO-Dynatrace AWS Elastic Loadbalancer \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_elastic\_loadbalancer\]

</td><td>

[Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Elastic Load Balancer

</td></tr><tr><td>

SGO-Dynatrace AWS Service Account

</td><td>

Ingests cloud service account data from Dynatrace.Contains information related to AWS account IDs.

</td><td>

SGO-Dynatrace AWS Service Account \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_service\_account\]

</td><td>

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AWS Credentials

</td></tr><tr><td>

SGO-Dynatrace Azure Load Balancer

</td><td>

Ingests Azure load balancer data from Dynatrace.Contains Azure load balancer and cloud load balancer IP address and tag details.

</td><td>

SGO-Dynatrace Azure Load Balancer \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_load\_balancer\]

</td><td>

[Cloud Load Balancer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Cloud LB IPAddress](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Azure Load Balancer

</td></tr><tr><td>

SGO-Dynatrace Azure Region

</td><td>

Ingests Azure datacenter data from Dynatrace.Contains Azure datacenter information.

</td><td>

SGO-Dynatrace Azure Region \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_region\]

</td><td>

[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Azure Region

</td></tr><tr><td>

SGO-Dynatrace Azure Storage Accounts

</td><td>

Ingests Azure cloud storage account data from Dynatrace.Contains information related to cloud storage accounts.

</td><td>

SGO-Dynatrace Azure Storage Accounts \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_storage\_accounts\]

</td><td>

[Cloud Storage Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Azure Storage Account

</td></tr><tr><td>

SGO-Dynatrace Azure Strg Acnts v2

</td><td>

Ingests Azure cloud storage account data from Dynatrace using v2 API.Contains information related to cloud storage accounts.

</td><td>

SGO-Dynatrace Azure Storage Accounts v2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_storage\_accounts\_v2\]

</td><td>

[Cloud Storage Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

cloud:azure:storage:storageaccounts

</td></tr><tr><td>

SGO-Dynatrace Azure Subscriptions

</td><td>

Ingests Azure subscription data from Dynatrace.Contains Azure subscription details.

</td><td>

SGO-Dynatrace Azure Subscriptions \[sn\_dynatrace\_integ\_sg\_dynatrace\_azure\_subscriptions\]

</td><td>

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Azure Subscription

</td></tr><tr><td>

SGO-Dynatrace Azure VM

</td><td>

Ingests Azure virtual machine instance data from Dynatrace.Contains information related to Azure virtual machine instances.

</td><td>

SGO-Dynatrace Azure VM \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_vm\]

</td><td>

[Virtual Machine Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Azure VM

</td></tr><tr><td>

SGO-Dynatrace Docker Container

</td><td>

Ingests Docker container data from Dynatrace.Contains information related to the Docker container image.

</td><td>

SGO-Dynatrace Docker Container \[sn\_dynatrace\_integ\_sgo\_dynatrace\_docker\_container\]

</td><td>

[Docker Container](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Docker Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Computer \[cmdb\_ci\_computer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Container Group Instance

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Cluster

</td><td>

Ingests Kubernetes cluster data from Dynatrace.Contains information related to Kubernetes clusters.

</td><td>

SGO-Dynatrace Kubernetes Cluster \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_cluster\]

</td><td>

[Kubernetes Cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Kubernetes Cluster

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Namespace

</td><td>

Ingests Kubernetes namespace data from Dynatrace.Contains information related to Kubernetes namespaces.

</td><td>

SGO-Dynatrace Kubernetes Namespace \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_namespace\]

</td><td>

[Kubernetes Namespace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Cloud Application Namespace

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Node

</td><td>

Ingests Kubernetes node data from Dynatrace.Contains information related to Kubernetes nodes.

</td><td>

SGO-Dynatrace Kubernetes Node \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_node\]

</td><td>

[Kubernetes Node](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Kubernetes Node

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Pod

</td><td>

Ingests Kubernetes pod data from Dynatrace.Contains information related to Kubernetes pods.

</td><td>

SGO-Dynatrace Kubernetes Pod \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_pod\]

</td><td>

[Kubernetes Pod](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Cloud Application Instance

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Service

</td><td>

Ingests Kubernetes service data from Dynatrace.Contains information related to Kubernetes services.

</td><td>

SGO-Dynatrace Kubernetes Service \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_service\]

</td><td>

[Kubernetes Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

Kubernetes Service

</td></tr><tr><td>

SGO-Dynatrace Azure Cosmos DB v1

</td><td>

Ingests Azure Cosmos DB data from Dynatrace. Contains information related to Azure Cosmos DB.

</td><td>

SGO-Dynatrace Azure Cosmos DB v1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_cosmos\_db\_v1\]

</td><td>

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AZURE\_COSMOS\_DB

</td></tr><tr><td>

SGO-Dynatrace Azure Cosmos DB V2

</td><td>

Ingests Azure Cosmos DB data from Dynatrace. Contains information related to Azure Cosmos DB.

</td><td>

SGO-Dynatrace Azure Cosmos DB V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_cosmos\_db\_v2\]

</td><td>

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

cloud:azure:documentdb:databaseaccounts:globalcloud:azure:documentdb:databaseaccounts:mongo

</td></tr><tr><td>

SGO-Dynatrace Azure SQL Server V2

</td><td>

Ingests Azure SQL Server data from Dynatrace. Contains information related to Azure SQL Server.

</td><td>

SGO-Dynatrace Azure SQL Server V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_sql\_server\_v2\]

</td><td>

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

cloud:azure:sql:servers:databases:dtucloud:azure:sql:servers:databases:vcore

cloud:azure:sql:servers:databases:hyperscale

</td></tr><tr><td>

SGO-Dynatrace Azure Function App

</td><td>

Ingests Azure Functions app data from Dynatrace. Contains information related to Azure Functions app.

</td><td>

SGO-Dynatrace Azure Function App \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_function\_app\]

</td><td>

[Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AZURE\_FUNCTION\_APP

</td></tr><tr><td>

SGO-Dynatrace Azure Scale Sets VM

</td><td>

Ingests Azure Virtual Machine Scale Sets \(VMSS\) data from Dynatrace. Contains information related to Azure VMSS.

</td><td>

SGO-Dynatrace Azure Scale Sets VM \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_scale\_sets\_vm\]

</td><td>

[Instance Scale Set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AZURE\_VM\_SCALE\_SET

</td></tr><tr><td>

SGO-Dynatrace AWS RDS V1

</td><td>

Ingests Amazon Relational Database Service \(RDS\) data from Dynatrace. Contains information related to Amazon RDS.

</td><td>

SGO-Dynatrace AWS RDS V1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_rds\_v1\]

</td><td>

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

RELATIONAL\_DATABASE\_SERVICE

</td></tr><tr><td>

SGO-Dynatrace AWS RDS V2

</td><td>

Ingests Amazon Relational Database Service \(RDS\) data from Dynatrace. Contains information related to Amazon RDS.

</td><td>

SGO-Dynatrace AWS RDS V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_rds\_v2\]

</td><td>

[Cloud DataBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

cloud:aws:rds

</td></tr><tr><td>

SGO-Dynatrace AWS Dynamo DB v1

</td><td>

Ingests Amazon Dynamo DB data from Dynatrace. Contains information related to Amazon Dynamo DB.

</td><td>

SGO-Dynatrace AWS Dynamo DB v1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_dynamo\_db\_v1\]

</td><td>

[DynamoDB Table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

DYNAMO\_DB\_TABLE

</td></tr><tr><td>

SGO-Dynatrace AWS Dynamo DB v2

</td><td>

Ingests Amazon Dynamo DB data from Dynatrace. Contains information related to Amazon Dynamo DB.

</td><td>

SGO-Dynatrace AWS Dynamo DB v2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_dynamo\_db\_v2\]

</td><td>

[DynamoDB Table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

cloud:aws:dynamodb

</td></tr><tr><td>

SGO-Dynatrace AWS Lambda Func V1

</td><td>

Ingests AWS Lambda Function data from Dynatrace. Contains information related to AWS Lambda Function.

</td><td>

SGO-Dynatrace AWS Lambda Func V1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_lambda\_func\_v1\]

</td><td>

[Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AWS\_LAMBDA\_FUNCTION

</td></tr><tr><td>

SGO-Dynatrace AWS Lambda Func V2

</td><td>

Ingests AWS Lambda Function data from Dynatrace. Contains information related to AWS Lambda Function.

</td><td>

SGO-Dynatrace AWS Lambda Func V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_lambda\_func\_v2\]

</td><td>

[Cloud Function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[Azure Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

cloud:aws:lambda

</td></tr><tr><td>

SGO-Dynatrace AWS S3 Bucket V2

</td><td>

Ingests Amazon S3 bucket data from Dynatrace. Contains information related to Amazon S3 bucket.

</td><td>

SGO-Dynatrace AWS S3 Bucket V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_s3\_bucket\_v2\]

</td><td>

[Cloud Object Storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

cloud:aws:s3

</td></tr><tr><td>

SGO-Dynatrace Custom Applications V2

</td><td>

Ingests custom application data from Dynatrace.Contains information related to custom applications.

</td><td>

SGO-Dynatrace Custom Applications \[sn\_dynatrace\_integ\_sgo\_dynatrace\_custom\_applications\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)Configuration Item \[cmdb\_ci\]

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

CUSTOM\_APPLICATION

</td></tr><tr><td>

SGO-Dynatrace AWS Auto Scaling Group V1

</td><td>

Ingests AWS autoscaling group data from Dynatrace using V1 API.Contains information related to AWS autoscaling group.

</td><td>

SGO-Dynatrace AWS Auto Scaling Group V1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_auto\_scaling\_group\_v1\]

</td><td>

[Cloud Resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)[AWS Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

[Key value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-dynatrace-classes.md)

</td><td>

AUTO\_SCALING\_GROUP

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

