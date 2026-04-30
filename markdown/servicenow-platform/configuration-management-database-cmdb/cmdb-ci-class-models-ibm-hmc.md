---
title: IBM Hardware Management Console \(HMC\) extension classes
description: The CMDB CI Class Models store app adds or updates classes for the IBM Hardware Management Console \(HMC\).
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# IBM Hardware Management Console \(HMC\) extension classes

The CMDB CI Class Models store app adds or updates classes for the IBM Hardware Management Console \(HMC\).

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can use the added classes as any other class. Applications such as Discovery and Service Mapping patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## IBM Hardware Management Console \(HMC\)

The IBM HMC extension classes support discovery of IBM virtualization technology by providing:

-   Discovery of LPARs/FRAMEs, which SAM use cases need
-   Topology data of IBM HMC, which event correlation requires
-   Topology data for ITSM use cases, such as in-frame migration

​

![IBM HMC extension classes integrated with the CMDB class hierarchy.](../image/IBM-HMC-CI-Class-Model.png "IBM HMC extension classes integrated with the CMDB class hierarchy")

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.3.0 adds the following classes for the IBM HMC. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_x53_n4v_phb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IBM Frame\[cmdb\_ci\_ibm\_frame\]

</td><td>

Server\[cmdb\_ci\_server\]

</td><td>

IBM physical machine with considerable resources which can be virtualized.

</td></tr><tr><td>

IBM HMC Processor pool\[cmdb\_ci\_processor\_pool\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

IBM shared pool used to allocate processors to a group of LPARs.

</td></tr></tbody>
</table>CMDB CI Class Models: Release 1.2.0 adds the following classes for the IBM HMC.

|Class|Extends|Description|
|-----|-------|-----------|
|IBM HMC Server \[cmdb\_ci\_hmc\_server\]|Server \[cmdb\_ci\_server\]|IBM console that manages frames and assigns logical partitions \(LPARs\) to pools.|
|IBM Frame \[cmdb\_ci\_ibm\_frame\]|Server \[cmdb\_ci\_server\]|IBM physical machine with considerable resources which can be virtualized.|
|IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\]|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|IBM logical partition representing the virtual aspect of the operating system.|
|LPAR Resource \[cmdb\_ci\_lpar\_resource\]|Configuration Item \[cmdb\_ci\]|Resource of an LPAR instance.|
|IBM HMC Processor pool \[cmdb\_ci\_processor\_pool\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|IBM shared pool used to allocate processors to a group of LPARs.|

## Class columns

CMDB CI Class Models: Release 1.3.0 adds the following columns to the respective classes.

|Added columns|Description|
|-------------|-----------|
|Current available processor units|Current available processor units.|
|Configurable processor units|Configurable processor units.|
|Configurable memory units|Configurable memory units.|
|Installed processor units|Installed processor units.|
|Current available memory units|Current available memory units.|
|Installed memory units|Installed memory units.|

|Added columns|Description|
|-------------|-----------|
|LPAR IDs|LPAR IDs.|
|LPAR names|LPAR names.|
|Frame name|Frame name.|

CMDB CI Class Models: Release 1.2.0 adds the following columns to the respective classes.

|Added columns|Description|
|-------------|-----------|
|Frame count|Count of frames.|

|Added columns|Description|
|-------------|-----------|
|Is VIO|Flags whether this VM is a \(VIO\) virtual input/output server in the HMC topology.|
|High Watermark VCPU|Peak in the utilization of virtual CPU assigned to during the reporting period.|
|Frame Serial Number|Serial number of a frame \(frame being a physical machine such as ESX\).|
|VIO Servers|List of VIO servers.|

|Added columns|Description|
|-------------|-----------|
|Node name|Name of the node.|
|Partition Name|Name of the partition.|
|Partition Number|Number of the partition.|
|Type|Type of LPAR Resource.|
|Mode|Mode of LPAR Resource.|
|Entitled Capacity|Allotted capacity granted.|
|Partition Group-ID|ID of a group of partitions.|
|Shared Pool ID|ID of a pool of shared processors.|
|Online Virtual CPUs|A virtual CPU.|
|Maximum Memory|Maximum amount of memory.|
|Minimum Memory|Minimum amount of memory.|
|Variable Capacity Weight|Logical partition processor capacity weight.|
|Minimum Capacity|Minimum number of processes.|
|Capacity Increment|Increments of process.|
|Maximum Physical CPUs in system|Maximum CPUs allotted in system.|
|Active Physical CPUs in system|Current CPUs in system.|
|Active CPUs in Pool|Number of active CPUs within a pool.|
|Shared Physical CPUs in system|Number of shared CPUs within a system.|
|Maximum Capacity of Pool|Maximum capacity of processes within a pool.|
|Entitled Capacity of Pool|Number of processes that are entitled.|
|Unallocated Capacity|Number of free spaces.|
|Physical CPU Percentage|Number of CPUs allocated to system.|
|Unallocated Weight|At no extra charge resources on instance.|
|Desired Virtual CPUs|Target number of virtual CPUs.|
|Desired Memory|Target amount of memory.|
|Desired Variable Capacity Weight|Targeted processor load.|
|Desired Capacity|Target resources used within instance.|
|High Watermark VCPU|Peak in the utilization of virtual CPU assigned to during the reporting period.|

|Added columns|Description|
|-------------|-----------|
|Pool ID|ID of pool of processors.|
|CPU Core count|Number of CPU cores.|
|Memory count|Amount of memory used.|
|Unassigned cores|Number of unused cores.|
|Unassigned memory|Amount of unassigned memory.|

The following class has no added columns: IBM Frame \[cmdb\_ci\_ibm\_frame\].

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

