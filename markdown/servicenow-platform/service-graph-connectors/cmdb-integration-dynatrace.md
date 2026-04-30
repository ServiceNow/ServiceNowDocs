---
title: Service Graph Connector for Observability - Dynatrace
description: Use the Service Graph Connector for Observability - Dynatrace to ingest CI data, events, metrics, and logs from Dynatrace into your ServiceNow instance.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-05"
reading_time_minutes: 10
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Observability - Dynatrace

Use the Service Graph Connector for Observability - Dynatrace to ingest CI data, events, metrics, and logs from Dynatrace into your ServiceNow instance.

**Note:** The Service Graph Connector for Observability - Dynatrace provided by ServiceNow is different from the Service Graph Connector for Dynatrace provided by Dynatrace.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported versions:
    -   Minimum version supported: Dynatrace SaaS; Version 1.284
-   Supported ServiceNow versions:
    -   Yokohama
    -   Zurich
    -   Australia

## Important information for upgrading Service Graph Connector for Observability - Dynatrace

Before upgrading the Service Graph Connector for Observability - Dynatrace to version 1.10.0 or later, disable the reconciliation rules for tables extending the Application \[cmdb\_ci\_appl\] table. See the [Reconciliation rules\(ServiceNow, ServiceWatch\) on multiple table like Apache web server stopping other discovery source to update fields on those tables \[KB1649455\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649455) article in the Now Support Knowledge Base.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for Observability - Dynatrace using SGC Central](../../sgc-central/task/sgcc-configure-dynatrace.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Dynatrace integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Dynatrace data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following table describes the data sources, the staging tables, the target tables as CMDB CI classes, and the Dynatrace entities imported by each data source.

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

[Computer](../reference/cmdb-dynatrace-classes.md#section_adv_nwg_jzb)[IP Address \[cmdb\_ci\_ip\_address\]](../reference/cmdb-dynatrace-classes.md#section_z34_5wg_jzb)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

When the Software Asset Management \(SAM\) application isn't installed:

[Software](../reference/cmdb-dynatrace-classes.md#section_ubs_zwg_jzb)

[Software Instance](../reference/cmdb-dynatrace-classes.md#section_cbx_dxg_jzb)

When the SAM application is installed: [Software Installation](../reference/cmdb-dynatrace-classes.md#section_o3b_cxg_jzb)

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

The target table is populated using Application Dependency Mapping \(ADM\). The ADM adapter analyzes the imported data and command-line arguments, identifies the appropriate table based on the conditions included in Discovery Process Classifications list, and inserts the data into the table, which extends the Application \[cmdb\_ci\_appl\] table. To learn about process classification, see [Discovery classifiers](https://www.servicenow.com/docs/access?context=discovery-classifiers&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

 **Note:** The addition of unclassified processes to the Application \[cmdb\_ci\_appl\] table depends on the value of the **sn\_dynatrace\_integ.createUnmatchedApplicationCIs** system property. For more information, see [Service Graph Connector for Observability - Dynatrace properties](../reference/sgc-cmdb-dynatrace-props.md).

</td><td>

Process

</td></tr><tr><td>

SGO-Dynatrace Process Groups V2

</td><td>

Ingests process group data from Dynatrace.Contains a group of similar running processes.

</td><td>

SGO-Dynatrace Process Groups \[sn\_dynatrace\_integ\_sg\_dynatrace\_process\_groups\]

</td><td>

[Group](../reference/cmdb-dynatrace-classes.md#section_cx4_5wg_jzb)

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

[Calculated Application Service](../reference/cmdb-dynatrace-classes.md#section_mlj_jwg_jzb)[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

[Application](../reference/cmdb-dynatrace-classes.md#id_i4z_125_tqb)

[Group](../reference/cmdb-dynatrace-classes.md#section_cx4_5wg_jzb)

[Computer](../reference/cmdb-dynatrace-classes.md#section_adv_nwg_jzb)

[Cloud Load Balancer](../reference/cmdb-dynatrace-classes.md#section_u1h_gwh_ldc)

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

[Calculated Application Service](../reference/cmdb-dynatrace-classes.md#section_mlj_jwg_jzb)[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

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

[Calculated Application Service](../reference/cmdb-dynatrace-classes.md#section_mlj_jwg_jzb)

</td><td>

Service

</td></tr><tr><td>

SGO-Dynatrace AWS Application Network LB

</td><td>

Ingests cloud load balancer data from Dynatrace.Contains information related to AWS application and network load balancer.

</td><td>

SGO-Dynatrace AWS Application Network LB \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_application\_network\_lb\]

</td><td>

[Cloud Load Balancer](../reference/cmdb-dynatrace-classes.md#section_u1h_gwh_ldc)[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

AWS Network Load BalancerAWS Application Load Balancer

</td></tr><tr><td>

SGO-Dynatrace AWS Datacenters

</td><td>

Ingests AWS datacenter and availability zone data from Dynatrace.Contains information related to AWS datacenters and availability zones.

</td><td>

SGO-Dynatrace AWS Availability Zone \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_availability\_zone\]

</td><td>

[AWS Datacenter](../reference/cmdb-dynatrace-classes.md#section_gpj_gwh_ldc)[Availability Zone](../reference/cmdb-dynatrace-classes.md#section_ry4_kwh_ldc)

</td><td>

AWS Availability Zone

</td></tr><tr><td>

SGO-Dynatrace AWS EC2 Instance

</td><td>

Ingests AWS virtual machine instance data from Dynatrace.Contains information related to virtual machine instances, server details, cloud hardware type, cloud image, and tags.

</td><td>

SGO-Dynatrace AWS EC2 Instance \[sn\_dynatrace\_integ\_sg\_dynatrace\_aws\_ec2\_instance\]

</td><td>

[Virtual Machine Instance](../reference/cmdb-dynatrace-classes.md#section_vmt_kwh_ldc)[Server](../reference/cmdb-dynatrace-classes.md#section_fjn_kwh_ldc)

[Cloud Hardware Type](../reference/cmdb-dynatrace-classes.md#section_mtl_kwh_ldc)

[Hardware Type](../reference/cmdb-dynatrace-classes.md#section_nhh_kwh_ldc)

[Image](../reference/cmdb-dynatrace-classes.md#section_x2f_gwh_ldc)

[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

EC2 Instance

</td></tr><tr><td>

SGO-Dynatrace AWS Elastic Loadbalancer

</td><td>

Ingests cloud load balancer data from Dynatrace.Contains load balancer details and tags.

</td><td>

SGO-Dynatrace AWS Elastic Loadbalancer \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_elastic\_loadbalancer\]

</td><td>

[Cloud Load Balancer](../reference/cmdb-dynatrace-classes.md#section_u1h_gwh_ldc)[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

Elastic Load Balancer

</td></tr><tr><td>

SGO-Dynatrace AWS Service Account

</td><td>

Ingests cloud service account data from Dynatrace.Contains information related to AWS account IDs.

</td><td>

SGO-Dynatrace AWS Service Account \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_service\_account\]

</td><td>

[Cloud Service Account](../reference/cmdb-dynatrace-classes.md#section_ld3_gwh_ldc)

</td><td>

AWS Credentials

</td></tr><tr><td>

SGO-Dynatrace Azure Load Balancer

</td><td>

Ingests Azure load balancer data from Dynatrace.Contains Azure load balancer and cloud load balancer IP address and tag details.

</td><td>

SGO-Dynatrace Azure Load Balancer \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_load\_balancer\]

</td><td>

[Cloud Load Balancer](../reference/cmdb-dynatrace-classes.md#section_u1h_gwh_ldc)[Cloud LB IPAddress](../reference/cmdb-dynatrace-classes.md#section_exj_kwh_ldc)

[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

Azure Load Balancer

</td></tr><tr><td>

SGO-Dynatrace Azure Region

</td><td>

Ingests Azure datacenter data from Dynatrace.Contains Azure datacenter information.

</td><td>

SGO-Dynatrace Azure Region \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_region\]

</td><td>

[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

</td><td>

Azure Region

</td></tr><tr><td>

SGO-Dynatrace Azure Storage Accounts

</td><td>

Ingests Azure cloud storage account data from Dynatrace.Contains information related to cloud storage accounts.

</td><td>

SGO-Dynatrace Azure Storage Accounts \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_storage\_accounts\]

</td><td>

[Cloud Storage Account](../reference/cmdb-dynatrace-classes.md#section_skk_gwh_ldc)

</td><td>

Azure Storage Account

</td></tr><tr><td>

SGO-Dynatrace Azure Strg Acnts v2

</td><td>

Ingests Azure cloud storage account data from Dynatrace using v2 API.Contains information related to cloud storage accounts.

</td><td>

SGO-Dynatrace Azure Storage Accounts v2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_storage\_accounts\_v2\]

</td><td>

[Cloud Storage Account](../reference/cmdb-dynatrace-classes.md#section_skk_gwh_ldc)

</td><td>

cloud:azure:storage:storageaccounts

</td></tr><tr><td>

SGO-Dynatrace Azure Subscriptions

</td><td>

Ingests Azure subscription data from Dynatrace.Contains Azure subscription details.

</td><td>

SGO-Dynatrace Azure Subscriptions \[sn\_dynatrace\_integ\_sg\_dynatrace\_azure\_subscriptions\]

</td><td>

[Cloud Service Account](../reference/cmdb-dynatrace-classes.md#section_ld3_gwh_ldc)

</td><td>

Azure Subscription

</td></tr><tr><td>

SGO-Dynatrace Azure VM

</td><td>

Ingests Azure virtual machine instance data from Dynatrace.Contains information related to Azure virtual machine instances.

</td><td>

SGO-Dynatrace Azure VM \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_vm\]

</td><td>

[Virtual Machine Instance](../reference/cmdb-dynatrace-classes.md#section_vmt_kwh_ldc)[Server](../reference/cmdb-dynatrace-classes.md#section_fjn_kwh_ldc)

</td><td>

Azure VM

</td></tr><tr><td>

SGO-Dynatrace Docker Container

</td><td>

Ingests Docker container data from Dynatrace.Contains information related to the Docker container image.

</td><td>

SGO-Dynatrace Docker Container \[sn\_dynatrace\_integ\_sgo\_dynatrace\_docker\_container\]

</td><td>

[Docker Container](../reference/cmdb-dynatrace-classes.md#section_l4q_kwh_ldc)[Application](../reference/cmdb-dynatrace-classes.md#id_i4z_125_tqb)

[Docker Image](../reference/cmdb-dynatrace-classes.md#section_xf5_bbp_bgc)

[Computer \[cmdb\_ci\_computer\]](../reference/cmdb-dynatrace-classes.md#section_adv_nwg_jzb)

</td><td>

Container Group Instance

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Cluster

</td><td>

Ingests Kubernetes cluster data from Dynatrace.Contains information related to Kubernetes clusters.

</td><td>

SGO-Dynatrace Kubernetes Cluster \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_cluster\]

</td><td>

[Kubernetes Cluster](../reference/cmdb-dynatrace-classes.md#section_qw3_gwh_ldc)[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

Kubernetes Cluster

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Namespace

</td><td>

Ingests Kubernetes namespace data from Dynatrace.Contains information related to Kubernetes namespaces.

</td><td>

SGO-Dynatrace Kubernetes Namespace \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_namespace\]

</td><td>

[Kubernetes Namespace](../reference/cmdb-dynatrace-classes.md#section_k1m_gwh_ldc)[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

Cloud Application Namespace

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Node

</td><td>

Ingests Kubernetes node data from Dynatrace.Contains information related to Kubernetes nodes.

</td><td>

SGO-Dynatrace Kubernetes Node \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_node\]

</td><td>

[Kubernetes Node](../reference/cmdb-dynatrace-classes.md#section_npq_nwh_ldc)[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

Kubernetes Node

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Pod

</td><td>

Ingests Kubernetes pod data from Dynatrace.Contains information related to Kubernetes pods.

</td><td>

SGO-Dynatrace Kubernetes Pod \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_pod\]

</td><td>

[Kubernetes Pod](../reference/cmdb-dynatrace-classes.md#section_sfv_kwh_ldc)[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

Cloud Application Instance

</td></tr><tr><td>

SGO-Dynatrace Kubernetes Service

</td><td>

Ingests Kubernetes service data from Dynatrace.Contains information related to Kubernetes services.

</td><td>

SGO-Dynatrace Kubernetes Service \[sn\_dynatrace\_integ\_sgo\_dynatrace\_kubernetes\_service\]

</td><td>

[Kubernetes Service](../reference/cmdb-dynatrace-classes.md#section_tbs_kwh_ldc)[Key Value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

Kubernetes Service

</td></tr><tr><td>

SGO-Dynatrace Azure Cosmos DB v1

</td><td>

Ingests Azure Cosmos DB data from Dynatrace. Contains information related to Azure Cosmos DB.

</td><td>

SGO-Dynatrace Azure Cosmos DB v1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_cosmos\_db\_v1\]

</td><td>

[Cloud DataBase](../reference/cmdb-dynatrace-classes.md#section_ylw_rp4_cfc)[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

[Cloud Service Account](../reference/cmdb-dynatrace-classes.md#section_ld3_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

AZURE\_COSMOS\_DB

</td></tr><tr><td>

SGO-Dynatrace Azure Cosmos DB V2

</td><td>

Ingests Azure Cosmos DB data from Dynatrace. Contains information related to Azure Cosmos DB.

</td><td>

SGO-Dynatrace Azure Cosmos DB V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_cosmos\_db\_v2\]

</td><td>

[Cloud DataBase](../reference/cmdb-dynatrace-classes.md#section_ylw_rp4_cfc)[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

[Cloud Service Account](../reference/cmdb-dynatrace-classes.md#section_ld3_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

cloud:azure:documentdb:databaseaccounts:globalcloud:azure:documentdb:databaseaccounts:mongo

</td></tr><tr><td>

SGO-Dynatrace Azure SQL Server V2

</td><td>

Ingests Azure SQL Server data from Dynatrace. Contains information related to Azure SQL Server.

</td><td>

SGO-Dynatrace Azure SQL Server V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_sql\_server\_v2\]

</td><td>

[Cloud DataBase](../reference/cmdb-dynatrace-classes.md#section_ylw_rp4_cfc)[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

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

[Cloud Function](../reference/cmdb-dynatrace-classes.md#section_ttj_gq4_cfc)[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

[Cloud Service Account](../reference/cmdb-dynatrace-classes.md#section_ld3_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

AZURE\_FUNCTION\_APP

</td></tr><tr><td>

SGO-Dynatrace Azure Scale Sets VM

</td><td>

Ingests Azure Virtual Machine Scale Sets \(VMSS\) data from Dynatrace. Contains information related to Azure VMSS.

</td><td>

SGO-Dynatrace Azure Scale Sets VM \[sn\_dynatrace\_integ\_sgo\_dynatrace\_azure\_scale\_sets\_vm\]

</td><td>

[Instance Scale Set](../reference/cmdb-dynatrace-classes.md#section_nsh_zn4_cfc)[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

[Cloud Service Account](../reference/cmdb-dynatrace-classes.md#section_ld3_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

AZURE\_VM\_SCALE\_SET

</td></tr><tr><td>

SGO-Dynatrace AWS RDS V1

</td><td>

Ingests Amazon Relational Database Service \(RDS\) data from Dynatrace. Contains information related to Amazon RDS.

</td><td>

SGO-Dynatrace AWS RDS V1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_rds\_v1\]

</td><td>

[Cloud DataBase](../reference/cmdb-dynatrace-classes.md#section_ylw_rp4_cfc)[AWS Datacenter](../reference/cmdb-dynatrace-classes.md#section_gpj_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

RELATIONAL\_DATABASE\_SERVICE

</td></tr><tr><td>

SGO-Dynatrace AWS RDS V2

</td><td>

Ingests Amazon Relational Database Service \(RDS\) data from Dynatrace. Contains information related to Amazon RDS.

</td><td>

SGO-Dynatrace AWS RDS V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_rds\_v2\]

</td><td>

[Cloud DataBase](../reference/cmdb-dynatrace-classes.md#section_ylw_rp4_cfc)[AWS Datacenter](../reference/cmdb-dynatrace-classes.md#section_gpj_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

cloud:aws:rds

</td></tr><tr><td>

SGO-Dynatrace AWS Dynamo DB v1

</td><td>

Ingests Amazon Dynamo DB data from Dynatrace. Contains information related to Amazon Dynamo DB.

</td><td>

SGO-Dynatrace AWS Dynamo DB v1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_dynamo\_db\_v1\]

</td><td>

[DynamoDB Table](../reference/cmdb-dynatrace-classes.md#section_lsd_yj4_cfc)[AWS Datacenter](../reference/cmdb-dynatrace-classes.md#section_gpj_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

DYNAMO\_DB\_TABLE

</td></tr><tr><td>

SGO-Dynatrace AWS Dynamo DB v2

</td><td>

Ingests Amazon Dynamo DB data from Dynatrace. Contains information related to Amazon Dynamo DB.

</td><td>

SGO-Dynatrace AWS Dynamo DB v2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_dynamo\_db\_v2\]

</td><td>

[DynamoDB Table](../reference/cmdb-dynatrace-classes.md#section_lsd_yj4_cfc)[AWS Datacenter](../reference/cmdb-dynatrace-classes.md#section_gpj_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

cloud:aws:dynamodb

</td></tr><tr><td>

SGO-Dynatrace AWS Lambda Func V1

</td><td>

Ingests AWS Lambda Function data from Dynatrace. Contains information related to AWS Lambda Function.

</td><td>

SGO-Dynatrace AWS Lambda Func V1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_lambda\_func\_v1\]

</td><td>

[Cloud Function](../reference/cmdb-dynatrace-classes.md#section_ttj_gq4_cfc)[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

AWS\_LAMBDA\_FUNCTION

</td></tr><tr><td>

SGO-Dynatrace AWS Lambda Func V2

</td><td>

Ingests AWS Lambda Function data from Dynatrace. Contains information related to AWS Lambda Function.

</td><td>

SGO-Dynatrace AWS Lambda Func V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_lambda\_func\_v2\]

</td><td>

[Cloud Function](../reference/cmdb-dynatrace-classes.md#section_ttj_gq4_cfc)[Azure Datacenter](../reference/cmdb-dynatrace-classes.md#section_igl_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

cloud:aws:lambda

</td></tr><tr><td>

SGO-Dynatrace AWS S3 Bucket V2

</td><td>

Ingests Amazon S3 bucket data from Dynatrace. Contains information related to Amazon S3 bucket.

</td><td>

SGO-Dynatrace AWS S3 Bucket V2 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_s3\_bucket\_v2\]

</td><td>

[Cloud Object Storage](../reference/cmdb-dynatrace-classes.md#section_smj_hm4_cfc)[AWS Datacenter](../reference/cmdb-dynatrace-classes.md#section_gpj_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

cloud:aws:s3

</td></tr><tr><td>

SGO-Dynatrace Custom Applications V2

</td><td>

Ingests custom application data from Dynatrace.Contains information related to custom applications.

</td><td>

SGO-Dynatrace Custom Applications \[sn\_dynatrace\_integ\_sgo\_dynatrace\_custom\_applications\]

</td><td>

[Calculated Application Service](../reference/cmdb-dynatrace-classes.md#section_mlj_jwg_jzb)Configuration Item \[cmdb\_ci\]

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

CUSTOM\_APPLICATION

</td></tr><tr><td>

SGO-Dynatrace AWS Auto Scaling Group V1

</td><td>

Ingests AWS autoscaling group data from Dynatrace using V1 API.Contains information related to AWS autoscaling group.

</td><td>

SGO-Dynatrace AWS Auto Scaling Group V1 \[sn\_dynatrace\_integ\_sgo\_dynatrace\_aws\_auto\_scaling\_group\_v1\]

</td><td>

[Cloud Resource](../reference/cmdb-dynatrace-classes.md#section_bkm_11p_bgc)[AWS Datacenter](../reference/cmdb-dynatrace-classes.md#section_gpj_gwh_ldc)

[Key value](../reference/cmdb-dynatrace-classes.md#section_o2r_ywg_jzb)

</td><td>

AUTO\_SCALING\_GROUP

</td></tr></tbody>
</table>When you complete setting up the connection, you can configure the integration to pull data from Dynatrace periodically. The data is loaded into the staging tables, and then inserted into the target tables.

For more information on where data is saved when pulling data from Dynatrace, see [CMDB classes targeted in Service Graph Connector for Observability - Dynatrace](../reference/cmdb-dynatrace-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Additional resources

-   [Introduction to Service Graph Connector for Observability Dynatrace](https://www.servicenow.com/community/cmdb-blog/introduction-to-service-graph-connector-for-observability/ba-p/2275131) article on the ServiceNow Community site
-   [How do I configure the Dynatrace Service Graph Connector?](https://www.servicenow.com/community/architect-articles/dynatrace-service-graph-connector/ta-p/2619549) article on the ServiceNow Community site

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

[Service Graph Connector for Observability - Dynatrace properties](../reference/sgc-cmdb-dynatrace-props.md)

