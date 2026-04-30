---
title: Service Graph Connector for Wiz
description: Use the Service Graph Connector for Wiz to ingest CMDB data from projects within the Wiz platform using the REST APIs.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-05"
reading_time_minutes: 5
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Wiz

Use the Service Graph Connector for Wiz to ingest CMDB data from projects within the Wiz platform using the REST APIs.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

-   Get started quickly with a streamlined onboarding process.
-   Use only the credentials you need.
-   Be instantly aware of any modifications with near real-time discovery of changes.
-   Get visibility across multiple cloud environments.
-   Identify risks in the environment through Wiz.
-   Assess application dependencies.
-   Get the most out of your security incident response and endpoint management with the ServiceNow AI Platform.

## Supported versions

<table id="table_kbm_ghs_2bc"><thead><tr><th>

Wiz

</th><th>

ServiceNow

</th></tr></thead><tbody><tr><td>

Last tested on February 20, 2026

</td><td>

-   Yokohama
-   Zurich
-   Australia

</td></tr></tbody>
</table>## Use cases

You can use the Service Graph Connector for Wiz to get visibility into cloud resource identities, relationships, and state in real-time.

## Configuring a connection

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Set up the Wiz environment](../task/sgc-cmdb-wiz-setup.md).

**Important:** Starting with the Service Graph Connector for Wiz version 1.4.0, the guided setup method is deprecated. Use the SGC Central view in the CMDB Workspace to configure the connection for the connector.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Wiz integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Wiz data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from the Wiz application.

**Note:** For any discovered resources that were deleted later, the Service Graph Connector for Wiz automatically marks the corresponding records as retired or absent in CMDB.

The following table lists the data sources, the staging tables, and the target tables CMDB CI classes and non-CMDB classes where data is stored for a Wiz project.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-Wiz-Organization

</td><td>

SG-Wiz-Organization \[sn\_wiz\_integ\_sg\_wiz\_organization\]

</td><td>

[Cloud Organizations](../reference/sgc-cmdb-wiz-classes.md#section_zbf_zgg_fxb)[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Google Organization Folder](../reference/sgc-cmdb-wiz-classes.md#section_tc1_gkk_bcc)

</td></tr><tr><td>

SG-Wiz-Subscription

</td><td>

SG-Wiz-Subscription \[sn\_wiz\_integ\_sg\_wiz\_subscription\]

</td><td>

[Cloud Service Account](../reference/sgc-cmdb-wiz-classes.md#section_o3z_5gg_fxb)[Google Organization Project](../reference/sgc-cmdb-wiz-classes.md#section_zqg_ydk_bcc)

[VMware vCenter Datacenter](../reference/sgc-cmdb-wiz-classes.md#section_www_5wq_2hc)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

SG-Wiz-Datacenter

</td><td>

SG-Wiz-Datacenter \[sn\_wiz\_integ\_sg\_wiz\_datacenter\]

</td><td>

[AWS Datacenter](../reference/sgc-cmdb-wiz-classes.md#section_q2s_5hg_fxb)[Azure Datacenter](../reference/sgc-cmdb-wiz-classes.md#section_qhy_tp5_vxb)

[Google Datacenter](../reference/sgc-cmdb-wiz-classes.md#section_uts_ffk_bcc)

[Logical Datacenter](../reference/sgc-cmdb-wiz-classes.md#section_wyc_zyq_2hc)

[OCI Datacenter](../reference/sgc-cmdb-wiz-classes.md#section_fky_bxq_2hc)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Resource-Group

</td><td>

SG-Wiz-Resource-Group \[sn\_wiz\_integ\_sg\_wiz\_resource\_group\]

</td><td>

[Resource Group](../reference/sgc-cmdb-wiz-classes.md#section_gdd_5lb_f1c)[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

SG-Wiz-Network-Interface

</td><td>

SG-Wiz-Network-Interface \[sn\_wiz\_integ\_sg\_wiz\_network\_interface\]

</td><td>

[Cloud Mgmt Network Interface](../reference/sgc-cmdb-wiz-classes.md#section_z4y_13g_fxb)[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

SG-Wiz-Virtual-Network

</td><td>

SG-Wiz-Virtual-Network \[sn\_wiz\_integ\_sg\_wiz\_virtual\_network\]

</td><td>

[Cloud Network](../reference/sgc-cmdb-wiz-classes.md#section_w2n_n4n_21c)[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

SG-Wiz-Firewall

</td><td>

SG-Wiz-Firewall \[sn\_wiz\_integ\_sg\_wiz\_firewall\]

</td><td>

[Compute Security Group](../reference/sgc-cmdb-wiz-classes.md#section_j4n_vhg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

SG-Wiz-Volume

</td><td>

SG-Wiz-Volume \[sn\_wiz\_integ\_sg\_wiz\_volume\]

</td><td>

[Storage Volume](../reference/sgc-cmdb-wiz-classes.md#section_ogm_nhg_fxb)[Cloud Disk Type](../reference/sgc-cmdb-wiz-classes.md#section_lmk_3rk_bcc)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

SG-Wiz-Virtual-Machine

</td><td>

SG-Wiz-Virtual-Machine \[sn\_wiz\_integ\_sg\_wiz\_virtual\_machine\]

</td><td>

[Virtual Machine Instance](../reference/sgc-cmdb-wiz-classes.md#section_fgm_hhg_fxb)

 [Hardware Type](../reference/sgc-cmdb-wiz-classes.md#section_wlb_1mk_bcc)

 [Cloud Hardware Type](../reference/sgc-cmdb-wiz-classes.md#section_ks5_ybr_2hc)

 [Linux Server](../reference/sgc-cmdb-wiz-classes.md#section_lzf_3p5_vxb)

 [Windows Server](../reference/sgc-cmdb-wiz-classes.md#section_rdg_xp5_vxb)

 [Server](../reference/sgc-cmdb-wiz-classes.md#section_y5x_yhg_fxb)

 [Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

 [SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Virtual-Machine-Image

</td><td>

SG-Wiz-Virtual-Machine-Image \[sn\_wiz\_integ\_sg\_wiz\_virtual\_machine\_image\]

</td><td>

[Image](../reference/sgc-cmdb-wiz-classes.md#section_c5r_cnb_f1c)

**Note:** Data with no subscription IDs for images aren't imported. Also, if the subscription ID for an image is available, but the subscription-specific details are not available in Wiz, the data isn't imported by the connector.

 [Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

 [SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Load Balancer

</td><td>

SG-Wiz-Load Balancer \[sn\_wiz\_integ\_sg\_wiz\_load\_balancer\]

</td><td>

[Cloud Load Balancer](../reference/sgc-cmdb-wiz-classes.md#section_ddq_2mb_f1c)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Database

</td><td>

SG-Wiz-Database \[sn\_wiz\_integ\_sg\_wiz\_database\]

</td><td>

[Cloud DataBase](../reference/sgc-cmdb-wiz-classes.md#section_mt2_flb_f1c)[Cloud DataBase Cluster](../reference/sgc-cmdb-wiz-classes.md#section_tmj_tmb_f1c)

[DynamoDB Table](../reference/sgc-cmdb-wiz-classes.md#section_tpv_skb_f1c)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Bucket

</td><td>

SG-Wiz-Bucket \[sn\_wiz\_integ\_sg\_wiz\_bucket\]

</td><td>

[Cloud Object Storage](../reference/sgc-cmdb-wiz-classes.md#section_gzl_5nb_f1c)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Serverless

</td><td>

SG-Wiz-Serverless \[sn\_wiz\_integ\_sg\_wiz\_serverless\]

</td><td>

[Cloud Function](../reference/sgc-cmdb-wiz-classes.md#section_o4k_qjb_f1c)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Network-Address

</td><td>

SG-Wiz-Network-Address \[sn\_wiz\_integ\_sg\_wiz\_network\_address\]

</td><td>

[Cloud Public IP Address](../reference/sgc-cmdb-wiz-classes.md#section_crz_h3s_g1c)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Storage-Account

</td><td>

SG-Wiz-Storage-Account \[sn\_wiz\_integ\_sg\_wiz\_storage\_account\]

</td><td>

[Cloud Storage Account](../reference/sgc-cmdb-wiz-classes.md#section_s1l_jgs_g1c)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-API-Gateway

</td><td>

SG-Wiz-API-Gateway \[sn\_wiz\_integ\_sg\_wiz\_api\_gateway\]

</td><td>

[Cloud Gateway](../reference/sgc-cmdb-wiz-classes.md#section_j2g_2s2_z1c)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Snapshot

</td><td>

SG-Wiz-Snapshot \[sn\_wiz\_integ\_sg\_wiz\_snapshot\]

</td><td>

[Storage Volume Snapshot](../reference/sgc-cmdb-wiz-classes.md#section_zkh_wgg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz Kubernetes Cluster

</td><td>

SG-Wiz Kubernetes Cluster \[sn\_wiz\_integ\_sg\_wiz\_k8s\_cluster\]

</td><td>

[Kubernetes Cluster](../reference/sgc-cmdb-wiz-classes.md#section_xzj_khg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz Kubernetes Namespace

</td><td>

SG-Wiz-K8s Namespace \[sn\_wiz\_integ\_sg\_wiz\_k8s\_namespace\]

</td><td>

[Kubernetes Namespace](../reference/sgc-cmdb-wiz-classes.md#section_gz4_lhg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Kubernetes Node

</td><td>

SG-Wiz-Kubernetes Node \[sn\_wiz\_integ\_sg\_wiz\_kubernetes\_node\]

</td><td>

[Kubernetes Node](../reference/sgc-cmdb-wiz-classes.md#section_vf1_dhg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Kubernetes Deployment

</td><td>

SG-Wiz-Kubernetes Deployment \[sn\_wiz\_integ\_sg\_wiz\_kubernetes\_deployment\]

</td><td>

[Kubernetes Deployment](../reference/sgc-cmdb-wiz-classes.md#section_hyk_1hg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Kubernetes Service

</td><td>

SG-Wiz-Kubernetes Service \[sn\_wiz\_integ\_sg\_wiz\_kubernetes\_service\]

</td><td>

[Kubernetes Service](../reference/sgc-cmdb-wiz-classes.md#section_kgl_mhg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Kubernetes Pod

</td><td>

SG-Wiz-Kubernetes Pod \[sn\_wiz\_integ\_sg\_wiz\_kubernetes\_pod\]

</td><td>

[Kubernetes Pod](../reference/sgc-cmdb-wiz-classes.md#section_rkm_1kg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Kubernetes Replica Set

</td><td>

SG-Wiz-Kubernetes Replica Set \[sn\_wiz\_integ\_sg\_wiz\_kubernetes\_replica\_set\]

</td><td>

[Kubernetes ReplicaSet](../reference/sgc-cmdb-wiz-classes.md#section_zdf_phg_fxb)[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz Kubernetes Container

</td><td>

SG-Wiz Kubernetes Container \[sn\_wiz\_integ\_sg\_wiz\_kubernetes\_container\]

</td><td>

[Docker Container](../reference/sgc-cmdb-wiz-classes.md#section_vx1_thg_fxb)[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

</td></tr><tr><td>

SG-Wiz-Compute Instance Group

</td><td>

SG-Wiz-Compute Instance Group \[sn\_wiz\_integ\_sg\_wiz\_compute\_instance\_group\]

</td><td>

[Instance Scale Set](../reference/sgc-cmdb-wiz-classes.md#section_xzs_ffd_dfc)[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr><tr><td>

SG-Wiz-Gateway

</td><td>

SG-Wiz-Gateway \[sn\_wiz\_integ\_sg\_wiz\_gateway\]

</td><td>

[Internet Gateway](../reference/sgc-cmdb-wiz-classes.md#section_xvp_t1r_2hc)[AWS Datacenter](../reference/sgc-cmdb-wiz-classes.md#section_q2s_5hg_fxb)

[SG-Wiz Extension Attributes](../reference/sgc-cmdb-wiz-classes.md#section_ldv_jds_zxb)

[Key Value](../reference/sgc-cmdb-wiz-classes.md#section_hbk_fhg_fxb)

</td></tr></tbody>
</table>**Note:** All the labels or tags associated with a Wiz resource are added to the Key Value \[cmdb\_key\_value\] table and the project information about a Wiz resource is stored in the SG-Wiz Extension Attributes \[sn\_wiz\_integ\_extension\_attributes\] table.

For more information on where data is saved when pulling data from a Wiz project, see [Target tables for storing Service Graph Connector for Wiz data](../reference/sgc-cmdb-wiz-classes.md) and [Supported Wiz types](../reference/sgc-cmdb-wiz-types.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

