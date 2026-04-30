---
title: Record removal process in Service Graph Connector for GCP
description: The Service Graph Connector for GCP uses soft deletion and hard deletion to manage the removal of records.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-10-12"
reading_time_minutes: 3
breadcrumb: [Reference, GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Record removal process in Service Graph Connector for GCP

The Service Graph Connector for GCP uses soft deletion and hard deletion to manage the removal of records.

Record removal is the process of handling data that is no longer needed. For any discovered resources that are deleted later after pulling data, the Service Graph Connector for GCP automatically updates the **Install Status** field of the associated CMDB CI classes to indicate any retired or deleted records.

-   [Soft deletion](sgc-cmdb-gcp-removal.md#section_dgn_plz_ncc)
-   [Hard deletion](sgc-cmdb-gcp-removal.md#section_lyp_bxh_cgc)

## Soft deletion

Soft deletion involves marking the install status of a record as **retired** rather than permanently deleting it from the system. The record remains in the database, making it possible to reference or restore it later.

Integration Commons Record Removal is implemented from Service Graph Connector for GCP version 1.11.0 to mark the Install Status and Operational Status of configuration items \(CIs\) as retired if they aren't discovered during the latest pull​. This implementation verifies the Last Scan attribute of the CIs in the Source \[sys\_object\_source\] table to identify CIs that aren't discovered during the latest pull​. Additionally, the source native keys \(SNKs\) for all CIs are modified to include the connection alias ID to identify the connection that discovered specific CIs.

Soft deletion for the Service Graph Connector for GCP 1.11.0 version relies on the Source \[sys\_object\_source\] table and the **Use Record Removal** and **lookback\_time\_in\_days** connection properties. Soft deletion for the Service Graph Connector for GCP 1.10 version and earlier relied on the SG-GCP Extension Attributes \[sn\_gcp\_integ\_extension\_attributes\] table.

After upgrading to version 1.11.0, the value of the **Use Record Removal** connection property is set to `true` when the import is run for the first time. Consequently, the latest SNKs for the CIs are included in the Source \[sys\_object\_source\] table. Record removal is implemented from the subsequent run.

After upgrading to version 1.11.0, the value of the **lookback\_time\_in\_days** connection property is set to null by default. During the initial run after the upgrade, the Source \[sys\_object\_source\] table is queried for all records that the connection discovered. By default, the value is set to 15 after the initial run. Two weeks after the initial run, the Source \[sys\_object\_source\] table is queried for all records that weren't discovered in the past 15 days. All records that weren't discovered in the past 15 days are marked as retired.

Soft deletion is enabled for the following data sources in Service Graph Connector for GCP:

-   SG-GCP Folder
-   SG-GCP Project
-   SG-GCP Network
-   SG-GCP Subnet
-   SG-GCP Storage Volume
-   SG-GCP Storage Volume Snapshot
-   SG-GCP Security Group
-   SG-GCP VM Instance
-   SG-GCP Load Balancer Pool
-   SG-GCP Load Balancer Pool Member
-   SG-GCP Load Balancer Health Service
-   SG-GCP Load Balancer
-   SG-GCP Load Balancer Service
-   SG-GCP Cloud Database
-   SG-GCP Cloud Function
-   SG-GCP Cloud Object Storage
-   SG-GCP Kubernetes Cluster
-   SG-GCP Kubernetes Node
-   SG-GCP Kubernetes Pod
-   SG-GCP Kubernetes Service
-   SG-GCP Kubernetes Namespace
-   SG-GCP Kubernetes Deployment
-   SG-GCP Kubernetes Replicaset
-   SG-GCP Kubernetes Cluster Roles
-   SG-GCP Kubernetes Cluster Role Binding
-   SG-GCP Kubernetes Node Pool

From Service Graph Connector for GCP version 1.10.0, the SG-GCP Generic Resource data source uses the post-script method for soft deletion, which relies on the Source \[sys\_object\_source\] table. For more information about the post-script method, see [Post-script method](cmdb-integ-record-removal.md#section_tkt_5cb_mbc).

## Hard deletion

Hard deletion involves permanently deleting a record from the system. The record is removed from the CMDB and can't be referenced or restored later. The SG-GCP Software Inventory data source uses the hard deletion method for the deletion of records.

**Parent Topic:**[Service Graph Connector for GCP reference](sgc-cmdb-gcp-reference.md)

**Related topics**  


[Service Graph Connector for GCP properties](../reference/cmdb-sgc-gcp-props.md)

