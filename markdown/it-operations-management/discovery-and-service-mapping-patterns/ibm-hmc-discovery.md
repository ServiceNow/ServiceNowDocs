---
title: IBM Virtualization and Hardware Management Console discovery
description: The Discovery and Service Mapping Patterns application uses the IBM HMC Server pattern to find information about Hardware Management Console \(HMC\), frame, and logical partition \(LPAR\) servers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM Virtualization and Hardware Management Console discovery

The Discovery and Service Mapping Patterns application uses the IBM HMC Server pattern to find information about Hardware Management Console \(HMC\), frame, and logical partition \(LPAR\) servers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery supports the following configuration items \(CIs\):

-   HMC server
-   IBM frame
-   LPAR instance

    An LPAR is the virtual machine equivalent of IBM.

-   LPAR resource

Discovery is used on the HMC server and the individual AIX machines \(LPARs\).

The IBM HMC Server pattern runs using SSH. It’s supported to run on IBM AIX OS for LPAR and on Linux for HMC servers only.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Verify permissions for HMC and AIX servers**
    -   Verify you have permissions for the following HMC commands:
        -   `lssyscfg`
        -   `lshmc`
        -   `lshwres`
        -   `lssysconn -r all -F type_model_serial_num:ipaddr`
    -   Verify you have permissions for the following AIX \(LPAR\) command: `lparstat -i`.

        **Note:** The `lparstat -i` command is in addition to the commands required for AIX server discovery. For more information on AIX server discovery, see [AIX server discovery](../../discovery/reference/r_DataCollDiscoAIXComputers.md). For a list of the AIX commands, see [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

-   **Configure SSH credentials**

    Configure SSH credentials on the ServiceNow AI Platform. For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Run a horizontal discovery for HMC Server and LPARs**

    1.  Run a discovery on the HMC IP address.
    2.  Only when the HMC Server discovery has successfully completed, run a discovery on the LPARs using the AIX machine IP address.
    For more information on running a discovery, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md#).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the IBM HMC Server pattern.

<table id="table_c2h_qgk_pdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the HMC.

</td></tr><tr><td>

Frame count \[frame\_count\]

</td><td>

Number of frames managed for the HMC.A frame is the physical machine on which the LPARs reside. A frame is the equivalent of an ESX machine.

</td></tr><tr><td>

Serial number \[serial number\]

</td><td>

Serial number of the HMC server.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the HMC.

</td></tr><tr><td>

OS Version \[os\_version\]

</td><td>

Operating system version.

</td></tr><tr><td>

CPU type \[cpu\_type\]

</td><td>

CPU type.

</td></tr><tr><td>

CPU speed \(MHz\) \[cpu\_speed\]

</td><td>

CPU speed.

</td></tr><tr><td>

CPU count \[cpu\_count\]

</td><td>

CPU count.

</td></tr><tr><td>

CPU core count \[cpu\_core\_count\]

</td><td>

CPU core count.

</td></tr><tr><td>

RAM \(MB\) \[ram\]

</td><td>

Memory RAM.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the frame.|
|Serial number \[serial number\]|Serial number of the Frame server.|
|Current available processor units \[curr\_avail\_sys\_proc\_units\]|Current available processor units.|
|Configurable processor units \[configurable\_sys\_proc\_units\]|Configurable processor units.|
|Installed processor units \[installed\_sys\_proc\_units\]|Installed processor units.|
|Current available memory units \[curr\_avail\_sys\_mem\]|Current available memory units.|
|Configurable memory units \[configurable\_sys\_mem\]|Configurable memory units.|
|Installed memory units \[installed\_sys\_mem\]|Installed memory units.|
|IP Address \[ip\_address\]|Management IP address of the IBM frame.|

<table id="table_u15_f1l_43b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the LPAR instance.

</td></tr><tr><td>

State \[state\]

</td><td>

Operational state. Possible values are On or Off.-   On: running
-   Off: not activated or not available

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Serial number of the LPAR.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique object identifier. This identifier is concatenated from the frame serial number and the LPAR identifier.

</td></tr><tr><td>

Is VIO \[is\_vio\]

</td><td>

Identifies the LPAR as a VIO server.A VIO server is the LPAR that manages the physical components for other LPARs, such as network interface cards \(NICs\) and optical drives.

</td></tr><tr><td>

VIO Servers \[vio\_servers\]

</td><td>

-   Client LPARs: Identifies the VIO servers that manage the client LPARs.
-   VIO servers: Identifies the Client LPARs the VIO servers manage.

</td></tr><tr><td>

Current Min Proc Units \[curr\_min\_proc\_units\]

</td><td>

Minimum number of processing units that can be assigned to the partition dynamically.

</td></tr><tr><td>

Running Proc Units \[run\_proc\_units\]

</td><td>

Number of processing units that are varied on for the partition.

</td></tr><tr><td>

Current Memory \[curr\_mem\]

</td><td>

The amount of memory in megabyte \(MB\) assigned to the partition.

</td></tr><tr><td>

Running Memory \[run\_mem\]

</td><td>

Current amount of memory in MB that the partition has varied on.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address assigned to the VIOS LPAR instance.

</td></tr><tr><td>

Model number \[model\_number\]

</td><td>

OS version of the VIOS LPAR instance.

</td></tr><tr><td>

Frame Name \[frame\_parent\]

</td><td>

References the IBM Frame \[cmdb\_ci\_ibm\_frame\] table.

</td></tr></tbody>
</table><table id="table_pzf_rgk_pdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

High Watermark VCPU \[high\_watermark\_vcpu\]

</td><td>

Highest recorded value of the **Online Virtual CPUs** field, as collected by the `lparstat-i` command. Because the value is dynamic, the results of a discovery could affect the value:

 -   If the value of the **Online Virtual CPUs** field is lower than the value collected by the `lparstat-i` command, the value doesn’t change.
-   If the value of the **Online Virtual CPUs** field is higher than the value collected by the `lparstat-i` command, the higher value is used.

</td></tr><tr><td>

Node name \[node\_name\]

</td><td>

Name of the instance, along with the field that refers to the LPAR instance CI.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Serial number \[serial\_number\]|Serial number of the CI.|

## CI Relationships

Discovery creates these relationships to support the IBM Virtualization and HMC discovery.

|CI|Relationship|CI|
|---|------------|---|
|IBM HMC Server \[cmdb\_ci\_hmc\_server\]|Defines resources for::Gets resources from|IBM HMC Processor Pool \[cmdb\_ci\_processor\_pool\]|
|IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\]|Virtualized by::Virtualizes|IBM Frame \[cmdb\_ci\_ibm\_frame\]|
|IBM Frame \[cmdb\_ci\_ibm\_frame\]|Managed by::Manages|IBM HMC Server \[cmdb\_ci\_hmc\_server\]|
|IBM HMC Processor Pool \[cmdb\_ci\_processor\_pool\]|Members::Member of|IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\]|
|IBM LPAR Instance \[cmdb\_ci\_lpar\_instance\]|References|IBM Frame \[cmdb\_ci\_ibm\_frame\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

