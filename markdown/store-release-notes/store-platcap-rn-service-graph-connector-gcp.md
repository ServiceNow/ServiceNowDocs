---
title: Service Graph Connector for GCP release notes
description: Version history for the Service Graph Connector for GCP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-gcp.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for GCP release notes

Version history for the Service Graph Connector for GCP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.13.0 - June 2026**
    -   New:
        -   Implemented new licensing model changes for Docker container.
        -   Implemented token reuse instead of generating tokens before an API call.
    -   Fixed:
        -   Resolved the issue where Kubernetes deployments were not being created because the parenttrimmed operation incorrectly truncated cluster names containing "k8s".
        -   Resolved the VM transformation failure caused by inconsistent data in the shieldedInstanceInitialState field during GCP virtual machine ingestion.
        -   Resolved the issue where the cmdb\_sam\_sw\_install records from SG-GCP incorrectly included architecture information in the version field.
-   **Version 1.12.0 - March 2026**
    -   New: The Project Number field is populated in the GCP Project \[cmdb\_ci\_gcp\_project\] table.
    -   Changed:
        -   The SG-GCP Organization parent import job for new connections has the Active option set to false by default.
        -   The parallel loading logic uses resource-type-based parallelism instead of account-based parallelism, improving data load performance in large-scale environments.
        -   Resource types aren't dynamically populated in the allowlist.
    -   Fixed:
        -   Source Native Keys \(SNKs\) use a connection alias for discovery.
        -   GCP virtual machines reflect the correct state.
        -   Default connection jobs don't display in the Multi Instance Setup Scheduled Import Jobs list.
        -   Kubernetes Pods don't experience memory issues during soft deletion.
        -   Key values aren't duplicated across Virtual Machine CIs.
        -   The Server name is updated when the VM Instance name changes.
        -   The Availability Zone and Implement Endpoint From VM fields are populated in the L1 relationship for the Storage Volume data source.
        -   Duplicate storage disk values are loaded without IRE payload errors.
        -   Soft deletion for Projects Discovery Scope is successful.
        -   Load errors don't lead to software removal.
        -   The performance of the Generic Resource job is improved.
        -   The Import Set Transformer query for the GCPRemoveSoftwareUtil script is optimized.
        -   The Discovery Credentials attribute mapping doesn't lead to horizontal discovery failures for GCP Cloud Discovery.
-   **Version 1.11.0 - October 2025**
    -   Fixed:
        -   Corrected the relationship mapping between GCP virtual machines \(VMs\) and their associated availability zones.
        -   Eliminated memory issues during GCP full data loads by offloading the comparison of current and retired CIs to the platform's record removal API.
    -   Changed: GCP full load mechanism: Updated the Source Native Key \(SNK\) configuration across 31 GCP data sources to include a connection alias, enabling the use of the core record removal API.
-   **Version 1.10.0 - August 2025**
    -   New:
        -   Deep discovery for Google Cloud: Explore and implement deep discovery for Google Cloud, similar to AWS Systems Manager, to run scripts on VM instances and pull detailed process, TCP, and middleware version information, in addition to already available installed software data.
        -   Labels and tags for generic CIs: Added support to bring in labels and tags for generic Configuration Items \(CIs\) in Google Cloud.
        -   Expanded CMDB Discovery for core infrastructure: Existing CMDB classes now support discovery for Google Cloud Network, Network ACL, NIC, OS Template, and VM instances.
        -   Deeper CMDB insights for cloud services and hierarchy: Enabled discovery for Endpoint Block, Endpoint VNIC, GCP Folder, GCP Project, Google Datacenter, Kubernetes Cluster, LB Pool, and LB Service CMDB classes.
        -   Granular CMDB discovery for foundational elements: Added new discovery capabilities for Availability Zone, Cloud Database, Service Account, Cloud Subnet, Compute Template, and Disk Type CMDB classes.
        -   Connection property for App Script filtering: Added a new connection property to filter App Script folders and projects.
    -   Fixed: Optimized generic resource design: Updated the generic resource design to no longer store API responses in memory, resolving the node restart and out of memory issues.
-   **Version 1.9.0 - May 2025**
    -   Changed:
        -   Updated table mappings for cloud hardware type and cloud OS image.
        -   Improved performance by changing the content type for list API calls to reduce the data size that is returned.
-   **Version 1.8.0 - February 2025**
    -   New:
        -   Improved connector to automatically discover and populate resource tags for all supported resource types.
        -   Implemented a Common Connection Framework for improved stability and efficiency.
        -   Populated the Parent attribute for GCP Folders with the corresponding parent Organization.
-   **Version 1.7.0 - October 2024**

    New: Added support for labels in GCP resources by implementing key-value mapping.

-   **Version 1.6.0 - September 2024**
    -   Fixed:
        -   Fixed the mappings for Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table in the SG-GCP Subnet data source
        -   Mapped Tags/Labels for Google Organization Project \[cmdb\_ci\_gcp\_project\] table.
        -   Fixed install\_status for Cloud DataBase \[cmdb\_ci\_cloud\_database\], Cloud Function \[cmdb\_ci\_cloud\_function\], Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\], Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\], and Kubernetes Node Pool \[cmdb\_ci\_kubernetes\_node\_pool\] tables
        -   Added install\_status/operational mapping for VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\] Block Endpoint \[cmdb\_ci\_endpoint\_block\], Storage Mapping \[cmdb\_ci\_storage\_mapping\], xIP Address \[cmdb\_ci\_ip\_address\]
        -   Fixed Volume ID field value in the Storage Volume \[cmdb\_ci\_storage\_volume\] class
        -   Fixed source native key for SG-GCP Network data source
-   **Version 1.5.0 - February 2024**
    -   New:
        -   Added support forKubernetes Node Pool, Kubernetes Cluster Roles, and Kubernetes Cluster Role Binding.
        -   Added the Advanced Setup section in the Guided Setup to synchronize data sources for upgrade scenarios.
        -   Updated the mappings in Kubernetes data sources - Kubernetes Cluster, Kubernetes Deployment, Kubernetes Node, Kubernetes Namespace, Kubernetes Pod, Kubernetes Replicaset, Kubernetes Service
        -   Populated configuration item in the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] class
-   **Version 1.4.0 - November 2023**
    -   New:
        -   Implemented bringing your own license \(BYOL\) that updates the license type in the Key Value \[cmdb\_key\_value\] table to analyze licenses.
        -   Added support for Discovery Redis, Memcache, Firestore, Cloud Big Table and Cloud Spanner- The details are populated in the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.
        -   Added ability to populate the generic cloud resources without CMDB classes in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.
        -   Added ability to update the Server \[cmdb\_ci\_server\] record with the Operating System, OS Version, RAM, Disk Space, CPU count, Is Virtual, and Object ID attributes.
        -   For any discovered software applications that were deleted later, the connector automatically deletes the corresponding records in CMDB.
        -   Added the Test the Connection task in the guided setup.
        -   Added ability to fetch active GCP resources only and filter out GCP resources with status as either terminated or suspended, or having transient states.
    -   Fixed:
        -   Restricted prefix to start with "sg-gcp" for multi-connections.
        -   Fixed the connection error displayed when running SG-GCP Hardware Type data source.
        -   Fixed the mapping for data from SG-GCP Cloud Function data source in the sn\_gcp\_integ\_extension\_attributes table.
        -   Fixed the import schedules with empty run-as option for multiple connections.
-   **Version 1.3.1 - August 2023**

    New:

    -   Added ability to populate installed software data for VMs
    -   Added support for ""Cloud Functions"", ""Cloud Load Balancer,"" and ""Cloud Database - SQL""
    Fixed:

    -   Fixed source native key for Key-Value table
    -   Corrected the import schedules to better support multi-instance
-   **Version 1.2.0 - May 2023**
    -   The Service Graph Connector for GCP enables cloud teams to integrate GCP data into the ServiceNow CMDB and ServiceNow workflows quickly, seamlessly, and securely. Designed with GCP security best practices and built on GCP Cloud Asset Inventory and pub/sub technologies. The Service Graph Connector for GCP automates access to populate multiple configuration classes, including virtual servers, network infrastructure, and installed software with minimal required credentials. Plug-and-play Service Graph Connectors simplify setup and facilitate quick improvements to business outcomes: reducing costs, automating processes, and optimizing the use of cloud resources.
    -   Key use cases:
        -   Visibility of Cloud resource identities, relationships, and statuses in near real-time
        -   A deep discovery of applications and software for Asset Management and Service Operations outcomes

