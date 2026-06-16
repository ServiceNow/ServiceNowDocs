---
title: Service Graph Connector for Microsoft Azure release notes
description: Version history for the Service Graph Connector for Microsoft Azure on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-ms-azure.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Microsoft Azure release notes

Version history for the Service Graph Connector for Microsoft Azure on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.17.0 - June 2026**
    -   New:
        -   Implemented the import of Microsoft/Websites.
        -   Implemented the automatic trigger of a full load using a schedule.
        -   Migrated the SG-Azure OS template to the Cloud OS image.
    -   Fixed:
        -   Resolved the issue where CPU count and CPU core count values were incorrectly populated, causing discrepancies in SAM licensing calculations.
        -   Corrected inconsistent Object ID formatting returned by the Azure API, which could lead to duplicate or mismatched records during ingestion.
        -   Addressed a NullPointerException in the SG-Azure Network Interface transform that occurred when the Name value was null during processing.
        -   Resolved a transformation failure in the SG-Azure Get Command when the Processes tag was missing from the API response.
        -   Corrected the Azure Functions Operational and Install Status mapping to properly handle null state values instead of producing errors.
        -   Addressed an incorrect data\_source\_id assignment in the SG-Azure Hardware Template after running the fix script in the SGC Azure version 1.15.0 plugin.
-   **Version 1.16.0 - March 2026**
    -   Changed: Resource types aren't dynamically populated in the allowlist.
    -   Fixed
        -   The Software Inventory data source runs successfully.
        -   The correct IP address is populated in the Computer \[cmdb\_ci\_computer\] and Server \[cmdb\_ci\_server\] tables.
        -   The SG-Azure Generic Resources full load is successful when the provisioningState property value is null.
        -   The Operational Status field populates Azure Kubernetes Cluster CIs.
        -   The storageContainerName and storageAccountName connection properties have distinct display names to avoid confusion during configuration.
        -   The Data Disk CIs populate relationships in the CMDB.
-   **Version 1.15.0 - December 2025**
    -   New:
        -   Added handling of custom page size properties for full-load operations, improving scalability and performance when syncing large sets of Azure resources.​
        -   Improved error handling for large payloads using attachment mechanisms, providing more reliable data processing and improved diagnostics during failures.​
    -   Changed: Modified network imports to fetch only required data from the Azure API, optimizing network resource synchronization and reducing unnecessary data transfer.​
    -   Fixed:
        -   Enhanced error handling for import operations affected by large payloads to provide more resilient data synchronization.
        -   Enhanced support for importing generic resources classified as Supported Resources to streamline imports and reduce irrelevant data ingestion.
-   **Version 1.14.0 - October 2025**
    -   New:
        -   Automated the prevention of ephemeral Azure Databricks VMs ingestion into the CMDB to reduce data bloat.
        -   Added support for flexible servers for enhanced functionality and user experience.
        -   Improved performance by moving data sources to Resource Graph API queries for full loads.
    -   Changed: Changed the SGC-Azure Network Interface data source to avoid partial API queries.
    -   Fixed:
        -   Resolved the issue where CIs were moved out of Retired status due to out-of-order processing.
        -   Resolved the issue where VM instances were created without an associated OS image.
        -   Resolved performance issues during datacenter updates caused by large database calls and high memory usage.
        -   Added support for large payloads for the Get Delta flow action.
        -   Resolved the issue where short-lived VMs were discovered despite setting the sn\_sg\_azure\_integ.insert\_short\_lived\_vmsproperty to false.
        -   Resolved the flip-flop issue in VDI classification when the power state is OFF.
        -   Resolved the lookback time issue where the lookback\_time\_in\_days property
-   **Version 1.13.0 - August 2025**
    -   New:
        -   Added Kubernetes discovery support for SGC Azure, providing a comprehensive view of cloud resources including cluster, account, and region information for Azure Kubernetes environments.
        -   Introduced a custom page size property for the Network data source.
    -   Changed:
        -   Enhanced the 'Create new connection' and 'Edit connection' flows in Azure SGC Central by adding new Pre-requisite and Properties steps.
        -   Implemented parallel loading for data sources in SG-Azure to improve performance.
        -   Enhanced the SG-Azure run command to automatically clean older testing run commands before execution.
    -   Fixed:
        -   Resolved the issue where OS information was not received for deallocated or terminated VMs, so that classification occurs only when the VM is in the 'on' state.
-   **Version 1.11.0 - February 2025**

    Changed: Implemented parallel loading for the Azure Virtual Machines, Network, and Storage Volumes data sources to reduce end-to-end loading time.

-   **Version 1.10.0 - November 2024**
    -   New:
        -   Improved data center ingestion for increased efficiency.
        -   Marks related NIC and storage volume as retired if scale set VM is retired.
    -   Fixed:
        -   Improved software pull query for large data sets in Log Analytics workspace.
        -   Correctly maps VDI servers to the Computer \[cmdb\_ci\_computer\] class based on the operating system type.
-   **Version 1.9.1 - September 2024**
    -   Fixed:
        -   Fixed connection name in the "Confirm connection creation" message \(Specific to SGC Central\)
        -   Software and Hardware connection names are non-editable \(Specific to SGC Central\)
-   **Version 1.9.0 - August 2024**
    -   New:
        -   Added support for software removal.
        -   Stopped pulling disabled subscriptions based on the sn\_sg\_azure\_integ.pull\_disabled\_subscriptions property value.
    -   Fixed:
        -   Mapped tags of the generic resource CIs to the Key Value \[cmdb\_key\_value\] table.
        -   Enhanced the delta pull performance by breaking the query into small chunks and improving the fault tolerance in delta pulls.
        -   Optimized API calls for the SG-Azure Scale Sets VMs data source.
        -   Disabled the SG-Azure VM Config Data data source for delta pulls.
        -   Removed the SG-Azure Server Config Data data source.
        -   Marked the SG-Azure Software import to inactive by default.
        -   Fixed HTTP 500 error for the SG-Azure Scale Sets data source. Fixed ClassCastException issue in the SG-Azure Generic Resources data source.
        -   Corrected life-cycle management for virtual machines \(VMs\) and servers.
        -   Fixed deletion process for Virtual Machine \(VM\) Scale Sets.
        -   Fixed issues with CIs being created with empty names in the SG-Azure Scale Sets data source.
-   **Version 1.7.3 - May 2024**
    -   Fixed:
        -   Handled HTTP 500 error for Scale Set API
        -   Fixed State and Install Status for scale set VMs
-   **Version 1.7.2 - March 2024**
    -   New:
        -   Manage the complete life cycle, including retirement, of Virtual Machine Scale Sets
        -   If a delta pull attempt fails, the Last Run Time value for a data source will no longer update
    -   Fixed:
        -   Improved the performance for delta pulls
        -   Fixed issues with importing deleted Azure Functions
        -   Fixed issues with importing tags for Azure Functions
        -   Added pagination for delta pulls
-   **Version 1.6.0 - February 2024**
    -   New:
        -   Populated IP address in VM and server classes.
        -   Added ability to populate the generic cloud resources without CMDB classes in the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.
        -   Added discovery for Azure Scale sets and Scale Sets virtual machines.
    -   Fixed:
        -   Fixed ClassCastException error on data transformation for VmConfig and Generic Resources.
        -   Fixed the problem for Test Load 20 records when subscriptions are more than 1000.
-   **Version 1.5.1 - January 2024**
    -   Fixed:
        -   Minor UI issue
        -   Plugin ACL/table misconfiguration issue
-   **Version 1.5.0 - November 2023**
    -   New:
        -   Added the SG-Azure Functions data source for discovering Azure functions.
        -   Added ability to fetch TCP and running process details.
    -   Fixed:
        -   Fixed test connection issue for multiple connections.
-   **Version 1.4.0 - July 2023**

    New:

    -   The "Configure an Azure policy for pulling software data of multiple VMs" topic on the ServiceNow documentation site is available for implementing role or policy in subscriptions to feed all virtual machines \(VMs\) data into a single Log Analytics workspace to pull software data
    -   Map SQL Server to the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table
    -   Import the Bring Your Own License \(BYOL\) licensing details from Windows and Linux servers
    Fixed:

    -   Issues related to support Azure Government cloud regions
-   **Version 1.3.0 - March 2023**
    -   New:
        -   Added server classifications for Windows and Linux
        -   Populated cloud bardware type table based on the parameter sn\_itom\_pattern.use a single hardware type for cloud datacenters
        -   Populated data center with cmdb\_ci\_azure\_datacenter table instead of cmdb\_ci\_logical\_datacenter
    -   Fixed: Optimized cloud hardware pull by using single subscription
-   **Version 1.2.1 - February 2023**

    Fixed: Fix the pagination issue for hardware import.

-   **Version 1.2.0 - December 2022**
    -   New:
        -   Pull cloud metadata and do deep discovery
        -   Importing Hardware CIs from Azure
        -   Azure Log Analytics Workspace API to get software information

