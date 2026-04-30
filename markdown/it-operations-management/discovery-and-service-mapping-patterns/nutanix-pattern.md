---
title: Nutanix Acropolis discovery
description: The ServiceNow Discovery application uses the Nutanix Components pattern to find components of the Nutanix Acropolis solution containing Nutanix Prism Central version 2024.3.1.8 or Nutanix Prism Element 7.0.1.6. The Nutanix VM Event pattern finds events created for virtual machines \(VMs\) in the Nutanix deployment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Nutanix Acropolis discovery

The ServiceNow Discovery application uses the Nutanix Components pattern to find components of the Nutanix Acropolis solution containing Nutanix Prism Central version 2024.3.1.8 or Nutanix Prism Element 7.0.1.6. The Nutanix VM Event pattern finds events created for virtual machines \(VMs\) in the Nutanix deployment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Nutanix Components pattern uses REST APIs to collect information about the Acropolis deployment components.

The Nutanix VM Event pattern runs every five minutes. If there are events that indicate the change of state in one of the Nutanix components, it triggers rediscovery of Nutanix components using the Nutanix Components Pattern.

Starting with version 1.29.0, Discovery and Service Mapping Patterns supports Nutanix v4 discovery. When you switch to v4, Discovery creates new pool and container records, while existing records stop being updated.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Verify MID Server requirements**

    Deploy and connect a dedicated MID Server with network access to Prism Element and Prism Central.

    To discover events related to VMs in the Nutanix deployment, set the MID Server capability to **All** or to **Nutanix**.

-   **Install Nutanix end-point SSL certificates for the MID Server JRE**
    1.  Collect the certificates by browsing the Nutanix Prism console on internet Explorer.
    2.  Add SSL certificates for the MID Server, as described in [Add SSL certificates for the MID Server](https://www.servicenow.com/docs/access?context=add-ssl-certificates&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    3.  Use the following JRE keytool command to import the SSL certificates in the MID Server's keystore: `<MID Installation>/jre/bin/keytool -import -v -keystore <MID Installation>jre/lib/security/cacerts`.

        If you must enter a password, enter the custom password or the default password- "changeit".

    4.  Install Nutanix end-point SSL certificates for the MID Server JRE.
-   **Verify API permissions for v1-3**

    Verify that the user has read-only access to the following API requests:

    -   `/PrismGateway/services/rest/v1/vms`
    -   `/PrismGateway/services/rest/v1/storage_pools`
    -   `/PrismGateway/services/rest/v2.0/tasks/list`
    -   `/PrismGateway/services/rest/v2.0/hosts`
    -   `/PrismGateway/services/rest/v2.0/clusters`
    -   `/PrismGateway/services/rest/v2.0/vms`
    -   `/PrismGateway/services/rest/v2.0/storage_containers`
    -   `/api/nutanix/v3/clusters/list`
    -   `/api/nutanix/v3/categories/list`
    -   `/api/nutanix/v3/categories/{category_keys}/list`
    -   `/api/nutanix/v3/category/query`
-   **Verify API permissions for v4**

    Verify that the user has read-only access to the following GET APIs. Note that the API call referencing `/PrismGateway/services/rest/v1/vms` uses a legacy endpoint because it's not available yet in the newer API.

    -   `/api/clustermgmt/v4/config/clusters`
    -   `/api/clustermgmt/v4/config/clusters/{clusters_ID}/hosts​`
    -   `/api/clustermgmt/v4/config/storage-containers`
    -   `/api/vmm/v4/ahv/config/vms`
    -   `/PrismGateway/services/rest/v1/vms`
    -   `/api/prism/v4/config/categories?$expand=associations​`
    -   `/api/prism/v4/config/categories/{categories_ID}?$limit=extId&$expand=detailedAssociations`
-   **Verify Prism Central version for v4 API**

    Ensure that Prism Central is at least version 7.3 to use the v4 API.

-   **Set MID Server property to discover v4**

    Enable Nutanix v4 discovery by setting MID Server property value to the exact v4 version. For more information, see [Enable Nutanix v4 discovery](../task/enable-nutanix-v4-discovery.md).

-   **Configure basic authentication credentials**

    For more information, see [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   **Create a serverless discovery schedule**

    Create a discovery schedule to perform targeted discovery of Nutanix components. For more information, see [Create a serverless schedule for Nutanix Acropolis discovery](../task/create-serverless-schedule-nutanix.md).

-   **Link Nutanix components to ESX clusters**

    The Nutanix Components pattern can discover Nutanix components hosted on ESX clusters, like storage pools, storage containers, and Controller Virtual Machine \(CVM\), but not ESX clusters themselves. Run VMware probe discovery before the Nutanix pattern discovery to link the Nutanix components to their ESX clusters. If you don't, the Nutanix components are linked to Nutanix Prism instead. For more information on VMware probe discovery, see [VMware discovery](../../discovery/concept/c_DiscoverVMwareInfrastructure.md).

-   **\(Optional\) Disable CI tag discovery**

    The Nutanix Components pattern discovers tags for Nutanix hosts and virtual machines. If you have dozens of tags in your deployment, it might slow down the discovery causing performance issues. You can disable the CI tag discovery by performing the following steps:

    1.  Navigate to **Pattern Designer** &gt; **Discovery Patterns**.
    2.  Select the **Nutanix Components** pattern.
    3.  Under **Extension Section**, select the check box for **Categories \(Tags\)** and select **Remove**.
    4.  Select **Save**.
-   **Adjust the batch size for removing redundant relationship data**

    The **sn\_itom\_pattern.nutanix\_relations\_deletion\_batch\_size** property sets the batch size for deleting relations between Nutanix Virtual Machine Instance and Nutanix Host. The default value is 1000; you can adjust this batch size as needed.


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Nutanix Components pattern.

**Note:** API v4 calls might retrieve or populate different values compared to v1-3. For more information, search the [Nutanix documentation](https://www.nutanix.dev/) for the "API Reference v4 Introduction" article.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Nutanix Controller VM.|
|VM ID \[vm\_id\]|The universally unique identifier \(UUID\) of the Nutanix Controller VM.|
|Object ID \[object\_id\]|The ID of the Nutanix Controller VM.|
|Memory \(MB\) \[memory\]|The memory size of the Nutanix Controller VM in Megabytes \(MB\).|
|State \[state\]|The power state of the Nutanix Controller VM \(on/off\).|
|Hypervisor Type \[hypervisor\_type\]|The type of the hypervisor used for the Nutanix Controller VM.|
|Description \[short\_description\]|The description defined for the virtual machine in the Nutanix console: Prism Central or Prism Element.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Nutanix Cluster.|
|IP Address \[ip\_address\]|The IP address of the Nutanix Cluster.|
|Cluster ID \[cluster\_id\]|The ID of the Nutanix Cluster.|
|Object ID \[object\_id\]|The object ID of the Nutanix Cluster.|
|Version \[version\]|The Nutanix Cluster version.|
|Full Version \[full\_version\]|The full version of the Nutanix Cluster.|
|Internal Subnet \[internal\_subnet\]|The subnet of the internal IP address of the Nutanix Cluster.|
|External Subnet \[external\_subnet\]|The subnet of the external IP address of the Nutanix Cluster.|
|Timezone \[timezone\]|The time zone of the Nutanix Cluster.|
|Hypervisor Types \[hypervisor\_types\]|The type of the hypervisor used for the Nutanix Cluster.|
|NTP Servers \[ntp\_servers\]|The Network Time Protocol \(NTP\) servers that are related to the Nutanix Cluster.|
|Number of Nodes \[num\_nodes\]|The number of nodes connected to the Nutanix Cluster.|
|NCC Version \[ncc\_version\]|The Nutanix Cluster Check \(NCC\) version.|
|Block Serial Numbers \[block\_serial\_numbers\]|The serial numbers of blocks of data connected to the Nutanix Cluster.|

<table id="table_u55_5fd_k2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name of the Nutanix host.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The ID of the Nutanix host.

</td></tr><tr><td>

CPU core count \[cpu\_core\_count\]

</td><td>

The number of Nutanix host cores.

</td></tr><tr><td>

CPU core thread \[cpu\_core\_thread\]

</td><td>

The number of threads of the Nutanix host.

</td></tr><tr><td>

CPU speed \(MHz\) \[cpu\_speed\]

</td><td>

The CPU speed of the Nutanix host in MHz.

</td></tr><tr><td>

CPU count \[cpu\_count\]

</td><td>

The number of CPU sockets of the Nutanix host.

</td></tr><tr><td>

RAM \(MB\) \[ram\]

</td><td>

The memory of the host in Megabites \(MB\).

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Serial number of the Nutanix host.This field is not applicable for v4.

</td></tr></tbody>
</table><table id="table_j3c_hgd_k2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

-   v1-3: The name of the Nutanix storage pool.
-   v4: Cluster name.

</td></tr><tr><td>

Pool ID \[pool\_id\]

</td><td>

-   v1-3: The UUID of the Nutanix storage pool.
-   v4: The external ID \(extId\) of the pool retrieved from the Nutanix Storage Container.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

-   v1-3: The ID of the Nutanix storage pool.
-   v4: The external ID \(extId\) of the pool retrieved from the Nutanix Storage Container.

</td></tr><tr><td>

Size \[size\]

</td><td>

The size of the Nutanix storage pool.This field is not applicable for v4.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The ID of the Nutanix container.|
|Container ID \[container\_id\]|The UUID of the Nutanix container.|
|Name \[name\]|The name of the Nutanix container.|
|Replication Factor \[replication\_factor\]|The number of copies created for the data stored on this Nutanix storage container.|
|Deduplication \[deduplication\]|The deduplication is enabled or disabled for the Nutanix container.|
|Compression \[compression\]|The compression is enabled or disabled for the Nutanix container.|
|Erasure Code \[erasure\_code\]|The erasure of code is enabled or disabled for the Nutanix container.|
|Size \[size\]|The Nutanix container size calculated dynamically during discovery.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the Nutanix Controller VM.|
|VM Instance ID \[vm\_inst\_id\]|The universally unique identifier \(UUID\) of the Nutanix Controller VM.|
|Object ID \[object\_id\]|The ID of the Nutanix Controller VM.|
|CPUs \[cpus\]|The number of CPUs that the VM has.|
|Memory \(MB\) \[memory\]|The memory size of the Nutanix Controller VM in Megabytes \(MB\).|
|State \[state\]|The power state of the Nutanix Controller VM \(on/off\).|
|Description \[short\_description\]|The description defined for the virtual machine in the Nutanix console: Prism Central or Prism Element.|

<table id="table_fkq_bjd_k2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The name of the Nutanix Prism Central multi-cluster manager.-   **PrismCentral@&lt;IP\_ADDRESS&gt;**: When the IP address is associated with the Prism Central instance, in the following scenarios:
    -   During quick discovery using HTTP classification.
    -   During serverless discovery if IP address was entered in **PRISM\_Address** parameter value.
-   **PrismCentral@&lt;DNS\_NAME&gt;**: When the DNS name is associated with the Prism Central instance and was entered in **PRISM\_Address** parameter value during serverless discovery.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The ID of the Nutanix Prism Central. This field has the same value as the **Name** field. -   **PrismCentral@&lt;IP\_ADDRESS&gt;**: When the IP address is associated with the Prism Central instance, in the following scenarios:
    -   During quick discovery using HTTP classification.
    -   During serverless discovery if IP address was entered in **PRISM\_Address** parameter value.
-   **PrismCentral@&lt;DNS\_NAME&gt;**: When the DNS name is associated with the Prism Central instance and was entered in **PRISM\_Address** parameter value during serverless discovery.

</td></tr></tbody>
</table>The graphic illustrates CIs that are part of the Acropolis discovery in deployments that use Nutanix AHV for virtualization.

![Nutanix components](../image/CheckResultNutanixAHV.png "Nutanix components")

The graphic illustrates CIs that are part of the Acropolis discovery in deployments that use VMware software for virtualization.

![Nutanix components in deployments using VMware software](../image/CheckResultNutanixVMware.png "Nutanix components in deployments using VMware software")

The graphic illustrates the Server and Nutanix VM Instance relationship.

![Server and Nutanix VM Instance relationship](../image/nutanix-vmi-server-relationship.png)

## CI relationships

These relationships are created to support all Nutanix discovery, regardless of hypervisor.

|CI|Relationship|CI|
|---|------------|---|
|Nutanix Cluster \[cmdb\_ci\_nutanix\_cluster\]|Members::Member of|Nutanix Host \[cmdb\_ci\_nutanix\_host\]|
|Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]|Registered::Has registered|Nutanix Host \[cmdb\_ci\_nutanix\_host\]|
|Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]|Hosted on::Hosts|Nutanix Cluster \[cmdb\_ci\_nutanix\_cluster\]|
|Nutanix Storage Pool \[cmdb\_ci\_nutanix\_storage\_pool\]|Contains::Contained by|Nutanix Storage Container \[cmdb\_ci\_nutanix\_storage\_container\]|
|Servers \[cmdb\_ci\_server\]|Instantiates::Instantiated by|Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]|
|Nutanix Cluster \[cmdb\_ci\_nutanix\_cluster\]|Managed by::Manages|Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\]|

These relationships are created to support Nutanix discovery for components hosted on AHV clusters.

|CI|Relationship|CI|
|---|------------|---|
|Nutanix Controller VM \[cmdb\_ci\_nutanix\_controller\_vm\]|Runs on::Runs|Nutanix Virtual Machine Instance \[cmdb\_ci\_nutanix\_vm\_instance\]|
|Nutanix Cluster \[cmdb\_ci\_nutanix\_cluster\]|Defines resources for::Gets resources from|Nutanix Storage Pool \[cmdb\_ci\_nutanix\_storage\_pool\]|

These relationships are created to support Nutanix discovery for components hosted on ESX clusters if you ran a VMware discovery.

|CI|Relationship|CI|
|---|------------|---|
|Nutanix Controller VM \[cmdb\_ci\_nutanix\_controller\_vm\]|Runs on::Runs|VMware Virtual Machine Instance \[cmdb\_ci\_vmware\_instance\]|
|VMware Cluster \[cmdb\_ci\_vmware\_cluster\]|Defines resources for::Gets resources from|Nutanix Storage Pool \[cmdb\_ci\_nutanix\_storage\_pool\]|

These relationships are created to support Nutanix discovery for components hosted on ESX clusters if you didn't run a VMware discovery.

|CI|Relationship|CI|
|---|------------|---|
|Nutanix Controller VM \[cmdb\_ci\_nutanix\_controller\_vm\]|Hosted on::Hosts|Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\]|
|Nutanix Storage Pool \[cmdb\_ci\_nutanix\_storage\_pool\]|Hosted on::Hosts|Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\]|

## Tag discovery

The Nutanix Components pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|The category key.|
|Value \[value\]|The category value.|
|Configuration item \[configuration\_item\]|References the Nutanix Host \[cmdb\_ci\_nutanix\_host\] table.|

## Dashboard

The dashboard contains reports that query the Configuration Management Database \(CMDB\) and display the results. The information is displayed only after the pattern has discovered the infrastructure.

To display the dashboard, navigate to **Self-Service** &gt; **Dashboards** &gt; **All** &gt; **Nutanix**.

After upgrading to Discovery Admin Workspace version 1.3.1 \(August 2024 Store\), you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the enhanced dashboard.

-   **[Enable Nutanix v4 discovery](../task/enable-nutanix-v4-discovery.md)**  
Enable Nutanix v4 discovery by setting the MID Server property value to the exact v4 version.

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

