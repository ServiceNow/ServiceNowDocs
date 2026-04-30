---
title: Discovery multiprobes and multisensors
description: Multiprobes contain one or more simple probes configured to extract specific information from manageable devices by executing multiple queries with a single authentication.You can add simple probes to your multiprobe in the Includes Probes related list.You can use the default multiprobes and multisensors provided in the platform or create your own.Create a multiensor to process data returned from a multiprobe.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery multiprobes and multisensors

Multiprobes contain one or more simple probes configured to extract specific information from manageable devices by executing multiple queries with a single authentication.

You can schedule multiprobes to run any time in the discovery process to make exploration more efficient. One common use for multiprobes is as [identity probes](../concept/c_HowDiscoveryIdentifiersWork.md). Identity probes ask a device for information such as its name and serial number, and then use the results of those queries to update existing CIs in the CMDB.

To process the data returned from a multiprobe, you must create multisensors, which run scripts that process the data returned by the multiprobes. Multisensors typically use the same name as their corresponding multiprobes.

**Note:** The corresponding multisensors have the same names as the multiprobes.

The following multiprobes are included with the base system.

<table id="table_qjm_yqv_tp"><thead><tr><th>

Multiprobe

</th><th>

Includes These Probes

</th></tr></thead><tbody><tr><td>

AIX - ADM

</td><td>

-   AIX - Active Processes: Gets active running processes.
-   Unix - Active Connections: Gets active connections information.

</td></tr><tr><td>

AIX - Identity

</td><td>

-   AIX - Network: Determines network interfaces, IPs, and MACs.
-   AIX - Serial Number: Gets AIX serial numbers.

</td></tr><tr><td>

CIM - Identity

</td><td>

CIM - Computer System: Gets CIM Computer Systems per SMI-S.

</td></tr><tr><td>

CIM - Identity - WBEM Service

</td><td>

CIM - CIMOM: Probes for the WBEM Service, CIMOM.

</td></tr><tr><td>

HP-UX - ADM

</td><td>

-   HP-UX - Active Processes: Gets active running processes.
-   Unix - Active Connections: Gets active connections information.

</td></tr><tr><td>

HP-UX - Identity

</td><td>

-   HP-UX - Hardware Serial Number: Gets HP-UX serial numbers.
-   HP-UX - Network: Determines network interfaces, IPs, and MACs.

</td></tr><tr><td>

Linux - Identity

</td><td>

-   Linux - Hardware Information: Gets DMI \(BIOS\) information.
-   Linux - Network: Determines network interfaces, IPs, and MACs.

</td></tr><tr><td>

Mac OS X - Identity

</td><td>

-   Mac OS X - Network: Determines network interfaces, IPs, and MACs.
-   Mac OS X - CPU/Memory: Gets CPU and memory information.

</td></tr><tr><td>

SNMP - A10 - Identity

</td><td>

-   SNMP - A10 - Identity - Serial: Part of the SNMP - Load Balancer - Identity multiprobe that is used to identify the A10 load balancer.
-   SNMP - Identity Info: Identifies an SNMP device.

</td></tr><tr><td>

SNMP - ACE - Identity

</td><td>

-   SNMP - Identity Info: Identifies an SNMP device.
-   SNMP - ACE - Identity - Serial: Part of the SNMP - Load Balancer - Identity multiprobe, that is used to identify the ACE load balancer

</td></tr><tr><td>

SNMP - Alteon - Identity

</td><td>

-   SNMP - Alteon - Identity - Serial: Part of the SNMP - Load Balancer - Identity multiprobe, that is used to identify the Alteon load balancer.
-   SNMP - Identity Info: Identifies an SNMP device.

</td></tr><tr><td>

SNMP - AppDirector - Identity

</td><td>

-   SNMP - AppDirector - Identity - Serial: Part of the SNMP - Load Balancer - Identity multiprobe, that is used to identify the AppDirector load balancer.
-   SNMP - Identity Info: Identifies an SNMP device.

</td></tr><tr><td>

SNMP - F5 BIG-IP - Identity

</td><td>

-   SNMP - F5 BIG-IP - Identity - Serial: Retrieves the BIG-IP chassis serial number, which is globally unique for this vendor.
-   SNMP - Identity Info: Identifies an SNMP device.

</td></tr><tr><td>

SNMP - Identity

</td><td>

SNMP - Identity Info: Identifies printer CIs

</td></tr><tr><td>

SNMP - Load Balancer - Identity

</td><td>

-   SNMP - F5 BIG-IP - Identity - Serial: Gets BIG-IP chassis serial numbers, which are globally unique for this vendor
-   SNMP - Identity Info: Identifies SNMP devices

</td></tr><tr><td>

SNMP - Netscaler - Identity

</td><td>

-   SNMP - Netscaler - Identity - Serial: Retrieves the Netscaler chassis serial number, which is globally unique for this vendor.
-   SNMP - Identity Info: Identifies SNMP devices

</td></tr><tr><td>

Solaris - ADM

</td><td>

-   Solaris - Active Processes: Gets active running processes
-   Unix - Active Connections: Gets active connections information

</td></tr><tr><td>

Solaris - Identity

</td><td>

-   Solaris - Network: Determines network interfaces, IPs, and MACs
-   Solaris - Serial Number: Gets serial numbers for Solaris devices †

</td></tr><tr><td>

Unix - ADM

</td><td>

-   Unix - Active Processes: Gets active running processes
-   Unix - Active Connections: Gets active connections information

</td></tr><tr><td>

UNIX - Classify

</td><td>

-   ESX - OS: Identifies ESX machines
-   UNIX - OS: Runs after the ESX - OS probe to determine the operating system for SSH devices not identified as ESX

</td></tr><tr><td>

Windows - ADM

</td><td>

-   Windows - Active Processes: Gets active running processes
-   Windows - Active Connections: Retrieves active connections information

</td></tr><tr><td>

Windows - Identity

</td><td>

-   Windows - Network: Determines network interfaces, IPs, and MACs
-   Windows - OS/Hardware Information: Probes a Windows machine for WMI information

</td></tr><tr><td>

Windows - Storage 2008

</td><td>

-   Windows - Storage 2008 - PS: Retrieves disk and file system information for Windows 2008 and earlier.
-   Windows - Storage 2008 - WMI: Retrieves disk and file system information for Windows 2008 and earlier.

</td></tr><tr><td>

Windows - Storage 2012

</td><td>

-   Windows - Storage 2012 - WMI: Retrieves disk and file system information for Windows 2012 and later.
-   Windows - Storage 2012 - PS: Retrieves disk and file system information for Windows 2012 and later.

</td></tr></tbody>
</table>**Note:** † This probe requires the installation of a command line tool from Oracle called SNEEP. To download and install this tool, log in to the [Oracle website](https://docs.oracle.com/cd/E35557_01/doc.81/e35226/ch3_sneep.htm). After this tool is installed, the **Solaris - Serial Number** probe runs automatically when Discovery detects a Solaris device. For Fujitsu PRIMEPOWER devices, you must run this probe with root credentials.

**Parent Topic:**[Discovery probes and sensors](../concept/c_DiscoveryProbesAndSensors.md)

## Add a simple probe to a multiprobe

You can add simple probes to your multiprobe in the Includes Probes related list.

### Before you begin

Role required: admin

### About this task

You can add simple probes of any type to a multiprobe and mix probe types if necessary.

**Warning:** Do not add a multiprobe to the Includes Probes related list.

### Procedure

1.  Navigate to **All** &gt; **Discovery Definitions** &gt; **Probes**.

2.  Open a multiprobe from the list.

    You can see the MultiProbe designation in the **ECC queue topic** column.

    ![Linux identity multiprobe form](../image/LinuxMultiProbe.png "Linux identity multiprobe")

3.  In the MultiProbe record, click **New** in the **Includes probes** related list.

4.  Select a simple probe from the collection list in the left column and move it into the included list..

    ![Adding a simple probe to a multiprobe](../image/AddSimpleProbe.png "Adding a simple probe to a multiprobe")

5.  Click **Save**.


## Create a Discovery multiprobe

You can use the default multiprobes and multisensors provided in the platform or create your own.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Definition** &gt; **Probes**.

2.  Click **New**.

3.  Complete the [form](r_Probes.md) using the following settings:

    -   Probe type: Multiprobe.
    -   ECC queue topic: MultiProbe.
4.  In the Includes probes related list, [add the probes](r_MultiprobesIncludedWithDiscovery.md#) you want to include in the multiprobe.

5.  Click **Save**.


## Create a Discovery multisensor

Create a multiensor to process data returned from a multiprobe.

### Before you begin

Role required: admin

### About this task

![Discovery Multisensor and Script](../image/DiscoveryMultisensorAndScript.png "Discovery Multisensor and Script")

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Definition** &gt; **Sensors**.

2.  Click **New**.

3.  Complete the form using the following settings:

    -   Sensor type: MultiSensor.
    -   ECC queue topic: MultiSensor.
    -   Reacts to probe: Select the probe whose payload this sensor must process.
    -   Sensor type: Select one of these options.
        -   Javascript: Returned data from the probe is processed in the sensor itself, outside the application, and is visible to the user. This is the most common sensor type.
        -   XML: The XML data from the probe is broken into pieces. Some pieces can be used to launch other probes that the original sensor needs to complete all the necessary information about a device.
4.  Right-click the form header, and click **Save**.

5.  In the Responds to Probes related list, click **New**.

6.  Complete the form using the following settings:

    -   Reacts to probe: Select the probe within the multiprobe that this sensor reacts to. The sensor must be linked to the probe by function, such as network identification or serial number.
    -   Script: Enter a script to run before the script in the multisensor. This script defines how the data returned from each probe should be processed.
7.  Click **Save**.


