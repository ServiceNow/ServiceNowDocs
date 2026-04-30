---
title: Oracle Linux Virtualization Manager and Red Hat Virtualization discovery
description: The ServiceNow Discovery application uses patterns to find Oracle Linux Virtualization Manager \(OLVM\) and Red Hat Virtualization \(RHV\) components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-11-09"
reading_time_minutes: 8
keywords: [Oracle Linux Virtualization Manager discovery, OLVM discovery, Oracle Linux Virtualization Manager patterns, OLVM patterns, Red Hat Virtualization discovery, Red Hat Virtualization patterns, RHV discovery, RHV patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Linux Virtualization Manager and Red Hat Virtualization discovery

The ServiceNow Discovery application uses patterns to find Oracle Linux Virtualization Manager \(OLVM\) and Red Hat Virtualization \(RHV\) components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Starting with version 1.28.0, Discovery and Service Mapping Patterns supports both OLVM and RHV discovery. Note that the RHV patterns, tables, and related items have been renamed to oVirt. For a full list of name changes, see the Zurich release [ITOM Visibility release notes](https://www.servicenow.com/docs/access?context=itom-visibility-rn&version=xanadu&pubname=xanadu-release-notes&ft:locale=en-US).

Discovery uses the following patterns for OLVM and RHV discovery:

-   oVirt Clusters and Hosts
-   oVirt Discover Logical Datacenters
-   oVirt Discover Manager Instance
-   oVirt Virtual Machines
-   oVirt Templates \(starting with Discovery and Service Mapping Patterns version 1.29.0\)

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Deploy the MID Server**

    Deploy and connect the dedicated MID Server to access either the OLVM or Red Hat Virtualization Manager \(RHV-M\) instances.

-   **Create oVirt credentials**

    Configure the following credentials:

    1.  Navigate to **Discovery** &gt; **Credentials**.
    2.  Select **New**.
    3.  Select **oVirt Credentials**, fill in the form, and then select **Submit**.

        |Field|Description|
        |-----|-----------|
        |Name|Credential name.|
        |User name|Name of the user for performing this discovery.|
        |Password|Password for this user.|
        |Active|Option to select to enable this credential for discovery.|
        |Bearer Token|Option to select to enable use of a bearer token.|

-   **Verify API permissions**

    Verify that the user has read-only permissions to send the following queries.

    -   /ovirt-engine/api/
    -   /ovirt-engine/api/datacenters
    -   /ovirt-engine/api/clusters
    -   /ovirt-engine/api/hosts
    -   /ovirt-engine/api/vms
    -   /ovirt-engine/api/disks
    -   /ovirt-engine/api/templates
    -   /ovirt-engine/api/networks
-   **Add CMDB CI Class Models**

    Add class models that extend the CMDB class hierarchy, using the CMDB CI Class Models application. The app is available from the ServiceNow Store. Discovery patterns use these class extensions to populate CIs. For more information, see [Red Hat Virtualization \(RHV\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-redhat-rhv&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **Create a cloud service account**

    Create an OLVM or RHV cloud service account on the ServiceNow instance.

    **Note:** Confirm that Discovery Admin Workspace is using at least version 1.10.0. The **Discovery** &gt; **Cloud Service Accounts** navigation module isn't available with earlier versions. To access **Cloud Service Accounts** with an earlier version, enter in the navigation filter: `cmdb_ci_cloud_service_account.list`.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Cloud Service Accounts**
    2.  Select **New**.
    3.  On the form, fill in the fields.

<table id="table_y3r_snq_vjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the service account.

</td></tr><tr><td>

Account Id

</td><td>

The account ID to which this credential belongs. The API url of the instance should be specified, including the port. For example: `https://my-manager-instance.com:443`.

</td></tr><tr><td>

Discovery credentials

</td><td>

The discovery credentials that were created previously.

</td></tr><tr><td>

Datacenter Type

</td><td>

The datacenter type, which should be oVirt LDC \[cmdb\_ci\_rhv\_ldc\].

</td></tr></tbody>
</table>-   **Create a discovery schedule**

    Create a discovery schedule to perform full discovery of OLVM or RHV components.

    1.  Open the cloud service account created previously.
    2.  Under **Related Links**, select **Create Discovery Schedule**.

        A new schedule is created under the **Discovery Schedule** menu item​.


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the patterns.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the datacenter.|
|Object ID \[object\_id\]|Unique object identifier.|
|Description \[short\_description\]|Description of the datacenter that you provide for easy identification.|
|Quota Mode \[quota\_mode\]|Quota mode policy.|
|URL \[url\]|API URL to access the datacenter.|
|Href ID \[href\_id\]|Href ID.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the cluster.|
|Object ID \[object\_id\]|Unique object identifier.|
|Description \[short\_description\]|Description of the cluster that you provide for easy identification.|
|CPU Type \[cpu\_type\]|CPU type. For example, x86\_64.|
|CPU Architecture \[cpu\_architecture\]|CPU architecture. For example, Intel Broadwell IBRS SSBD MDS Family.|
|KSM \[ksm\]|Enabled state of kernel same-page merging \(KSM\) memory policy.|
|Fencing Policy \[fencing\_policy\]|Fencing policy.|
|Memory Overcommit \[memory\_overcommit\]|Amount of over-commitment memory allowed on the cluster.|
|Transparent Huge Pages \[thp\]|Transparent huge memory pages policy.|
|Ballooning \[ballooning\]|Memory ballooning for guests.|
|Compatability Version \[compatibility\_version\]|Compatibility version.|
|URL \[url\]|API URL to access the cluster.|
|Href ID \[href\_id\]|Href ID.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the server.|
|Serial number \[serial\_number\]|Serial number.|
|Object ID \[object\_id\]|Unique object identifier.|
|CPU core count \[cpu\_core\_count\]|Total number of cores.|
|CPU count \[cpu\_count\]|Total number of CPUs.|
|CPU type \[cpu\_type\]|CPU type.|
|CPU speed \(MHz\) \[cpu\_speed\]|CPU speed \(MHz\).|
|Host name \[host\_name\]|Hostname.|
|IP Address \[ip\_address\]|IP address of the server.|
|Model ID \[model\_id\]|Model ID.|
|Operating System \[os\]|OS family.|
|OS Version \[os\_version\]|OS version.|
|RAM \(MB\) \[ram\]|Amount of RAM \(MB\).|
|URL \[url\]|API URL used access the server.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the instance.|
|State \[state\]|State of the instance.|
|Object ID \[object\_id\]|Unique object identifier.|
|IP Address \[ip\_address\]|IP address of the instance.|
|Disks \[disks\]|Number of disks.|
|MAC Address \[mac\_address\]|MAC address of the instance.|
|Management URL \[mgmt\_url\]|Management API URL.|
|Description \[short\_description\]|Description of the instance that you provide for easy identification.|
|Fully qualified domain name \[fqdn\]|Fully Qualified Domain Name \(FQDN\) of the instance.|
|CPU Architecture \[cpu\_architecture\]|CPU architecture. For example: Intel Broadwell IBRS SSBD MDS Family.|
|Delete Protected \[delete\_protected\]|Delete protected, possible values: true or false.|
|CPUs \[cpus\]|Number of CPUs.|
|HA Priority \[ha\_priority\]|High availability \(HA\) priority.|
|High Availability \[high\_availability\]|High availability, possible values: true or false.|
|Memory MAX \[memory\_policy\_max\]|Maximum memory in the dynamic memory allocation policy for the virtual machine \(VM\).|
|Memory Guarantee \(MB\) \[memory\_policy\_guaranteed\]|Amount of memory guaranteed for the VM \(MB\).|
|Multi Queues \[multi\_queues\]|Multi queues.|
|Placement Policy \[placement\_policy\]|Placement policy.|
|Stateless \[stateless\]|Stateless, possible values: true or false.|
|On Storage Error \[storage\_error\_resume\_behaviour\]|Behavior of a VM that is paused due to storage I/O error. For example: AUTO\_RESUME, LEAVE\_PAUSED, and KILL.|
|Start Time \[start\_time\]|Start time of the VM.|
|Stop Time \[stop\_time\]|Stop time of the VM.|
|Threads \[threads\]|Number of threads.|
|Time Zone \[time\_zone\]|Time zone of the VM.|
|USB \[usb\]|USB enabled state.|
|Run Once \[run\_once\]|Run once.|
|RHV Type \[rhv\_type\]|OLVM or RHV type.|

|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|Account ID for this cloud service account.|
|Object ID \[object\_id\]|Account ID for this cloud service account.|
|Datacenter Type \[datacenter\_type\]|Type of datacenter: oVirt LDC \[cmdb\_ci\_rhv\_ldc\].|
|Discovery credentials \[discovery\_credentials\]|Credentials for this cloud service account.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The IP address of the network interface card \(NIC\) assigned to the VM.|
|IP Address \[ip\_address\]|The IP address of the NIC assigned to the VM.|
|IP version \[ip\_version\]|IP version: IPv4 or IPv6.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique identifier for this resource.|
|Name \[name\]|Name for the virtual network interface card \(vNIC\) endpoint.|
|IP Address \[ip\_address\]|IP address bound to the network interface.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|ID of the network interface.|
|Name \[name\]|Name of the network interface.|
|IP Address \[ip\_address\]|IP address bound to the network interface.|
|Public IP \[public\_ip\]|Public IP address bound to the network interface.|
|Private IP \[private\_ip\]|Private IP address bound to the network interface.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the disk.|
|Object ID \[object\_id\]|Unique ID of the disk.|
|Size \[size\]|Storage capacity of the disk.|
|Storage type \[storage\_type\]|Type of storage backend the disk is using.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the network.|
|Object ID \[object\_id\]|Unique ID of the network.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the template.|
|Object ID \[object\_id\]|Unique ID of the template.|
|Cores \[cores\]|Number of CPU cores.|
|Install Status \[install\_status\]|Install status of the template. Default value is Installed.|
|Memory MB \[memory\_mb\]|Memory in megabytes \(MB\).|

On the Dependency Views map, you can view all discovered OLVM or RHV resources in your organization and the relationships between them.

![OLVM or RHV CIs and connections on a Dependency Views map](../image/ovirt-dependency-view.png "OLVM or RHV dependency view")

## CI relationships

The following relationships are created to support OLVM or RHV discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\]|Hosted on::Hosts|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Extends from|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Extends from|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Extends from|Configuration Item \[cmdb\_ci\]|
|oVirt Cluster \[cmdb\_ci\_rhv\_cluster\]|Members::Member of|oVirt Server \[cmdb\_ci\_rhv\_server\]|
|oVirt Cluster \[cmdb\_ci\_rhv\_cluster\]|Extends from|oVirt Object \[cmdb\_ci\_rhv\_object\]|
|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|Contains::Contained by|oVirt Cluster \[cmdb\_ci\_rhv\_cluster\]|
|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|Extends from|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|oVirt Server \[cmdb\_ci\_rhv\_server\]|Runs on::Runs|Linux Server \[cmdb\_ci\_linux\_server\]|
|oVirt Server \[cmdb\_ci\_rhv\_server\]|Extends from|Virtualization Server \[cmdb\_ci\_virtualization\_server\]|
|oVirt Virtual Machine Instance \[cmdb\_ci\_rhv\_vm\_instance\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|oVirt Virtual Machine Instance \[cmdb\_ci\_rhv\_vm\_instance\]|Hosted on::Hosts|oVirt Cluster \[cmdb\_ci\_rhv\_cluster\]|
|oVirt Virtual Machine Instance \[cmdb\_ci\_rhv\_vm\_instance\]|Hosted on::Hosts|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|
|oVirt Virtual Machine Instance \[cmdb\_ci\_rhv\_vm\_instance\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|oVirt Virtual Machine Instance \[cmdb\_ci\_rhv\_vm\_instance\]|Registered on::Registers|oVirt Server \[cmdb\_ci\_rhv\_server\]|
|oVirt Virtual Machine Instance \[cmdb\_ci\_rhv\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|oVirt Virtual Machine Instance \[cmdb\_ci\_rhv\_vm\_instance\]|Extends from|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|oVirt LDC \[cmdb\_ci\_rhv\_ldc\]|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Extends from|Endpoint \[cmdb\_ci\_endpoint\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

