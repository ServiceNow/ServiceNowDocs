---
title: Discovery probes and sensors
description: Discovery probes and sensors perform data collection and update the CMDB.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery probes and sensors

Discovery probes and sensors perform data collection and update the CMDB.

With each release, patterns are replacing many probes and sensors for Discovery. Consider creating new patterns or editing existing ones if you want to customize what Discovery can find. The information on probes and sensors is intended for customers who are not using patterns yet and for customers who already have customized probes that are retained upon upgrade. See [Patterns and horizontal discovery](c-UsingPatternsForHorizontalDiscovery.md#) for more information on patterns.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Discovery phases

Discovery always uses probes and sensors during the first two phases of discovery: scanning and classification. For the last two phases, identification and exploration, Discovery can use probes and sensors or patterns. This topic refers to probes and sensors only. See [Exploring Discovery](c_GetStartedWithDiscovery.md) for an explanation of these phases. See [Patterns and horizontal discovery](c-UsingPatternsForHorizontalDiscovery.md#) for more information on patterns.

## Probes, sensors, and the ECC queue

The probe collects the information and the sensor processes it. Both get their instructions from the ECC queue. There is a worker job on the MID Server that monitors the queue for work. The monitor checks for any entries where the Queue is output and the State is ready.

![The ECC queue](../image/ECCQueueOutput.png)

The MID Server then processes all the output ECC messages, runs the necessary probes, and returns the probes results to the ECC queue. These results are put in the ECC Queue as input entries.

![ECC queue record](../image/ECCQueueInput.png "ECC queue input")

After an entry is inserted in the ECC Queue table, a business rule fires \(on insert\) that takes that information and runs it through a sensor processor. The sensor processor's job is to take the input data, find any sensors interested in that data, and pass it along to be processed. Those sensors ultimately update the CMDB.

## How probes and sensors work together

The MID Server launches probes to collect information about a device. The probe sends back information to the sensor to be processed. If the probe has a post-processing script defined, the post-processing script does some data processing on the MID Server before data is sent back to the sensor on the ServiceNow instance. Otherwise the probes sends back all the data collected and the sensor performs this data processing. In both cases, the sensor updates the CMDB.

A multi-probe is a probe that contains probes. A multi-sensor processes the data from a multi-probe. To process the data from the multi-probe, the multi-sensor contains individual scripts to process the data returned by each probe contained in the Multiprobe, as well as a main multi-sensor script. The individual scripts pass their processed data to the main multi-sensor script.

![The MultiSensor form](../image/MultisensorExample.png)

## Probe types

<table id="table_ixz_r1l_z4"><thead><tr><th>

Device

</th><th>

Probe Type

</th></tr></thead><tbody><tr><td>

Windows

 computers and servers

</td><td>

Remote WMI queries, shell commands

</td></tr><tr><td>

UNIX and Linux servers

</td><td>

Shell command \(via SSH protocol, version 2\). Discovery supports any Bourne-compatible shell.

</td></tr><tr><td>

Storage

</td><td>

CIM/WBEM queries

</td></tr><tr><td>

Printers

</td><td>

SNMP queries

</td></tr><tr><td>

Network gear \(switches, routers, etc.\)

</td><td>

SNMP queries

</td></tr><tr><td>

Web servers

</td><td>

HTTP header examination

</td></tr><tr><td>

Uninterruptible Power Supplies \(UPS\)

</td><td>

SNMP queries

</td></tr></tbody>
</table>-   **[List of Discovery probes](../reference/r_ListOfDiscoveryProbes.md)**  
A wide variety of probes exist for the Discovery application to detect elements on your network.
-   **[Discovery sensors](../reference/r_Sensors.md#)**  
Every probe in Discovery must have a corresponding sensor to process the data returned.
-   **[Discovery probe management](../reference/r_Probes.md)**  
Several discovery probes and their associated sensors are included with Discovery. You rarely need to modify probes or sensors. But you might need to set parameters to control the behavior of a particular probe or align versions of customized probes.
-   **[Align versions of customized probes and sensors](../task/t_AlignVerCustProbeSens.md)**  
If you customized a probe or sensor and upgraded to a new version of an instance, you need to realign the versions of the customized probe and sensor to the most current version.
-   **[Discovery multiprobes and multisensors](../reference/r_MultiprobesIncludedWithDiscovery.md#)**  
Multiprobes contain one or more simple probes configured to extract specific information from manageable devices by executing multiple queries with a single authentication.
-   **[Example custom Discovery probe and sensor: populate a CI with text file values](../../../script/server-scripting/task/t_CustomProbeTextFile.md)**  
This custom Discovery probe helps you if you need to read a text file from a Windows computer and populate a CI in the CMDB with the values from the file.

**Parent Topic:**[Discovery](../reference/r-discovery.md)

