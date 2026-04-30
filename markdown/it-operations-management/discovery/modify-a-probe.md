---
title: Create or modify a probe
description: Create a new probe to discover additional CIs or modify an existing probe to collect additional information. After you create or modify a probe, test it.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Discovery probe management, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create or modify a probe

Create a new probe to discover additional CIs or modify an existing probe to collect additional information. After you create or modify a probe, test it.

## Before you begin

Role required: admin

**Important:** You need an advanced knowledge of scripting to modify probes or their associated sensors. Many existing probes provide parameters that you can set, rather than modifying the probe itself. See [Set probe parameters](t_SetProbeParameters.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Definition** &gt; **Probes**.

2.  Click the name of the probe that you want to modify.

3.  Modify the form fields \(see table\).

<table id="table_k53_2dv_tp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Class

</td><td>

Select the probe for the operating system of the device it will query.-   AWS Probe: Select this class to query your resources inside an AWS cloud.
-   [**CIM Probe**](../reference/r_CIMProbe.md#): Select this probe type to query a CIM server using WBEM protocols.
-   [**Multiprobe**](../reference/r_MultiprobesIncludedWithDiscovery.md#): Select this probe type to run one or more simple probes of any type or mix probes of different types. This type of probe can make several queries simultaneously that return all the results at the same time. You cannot add multiprobes to other multiprobes.
-   **Probe**: Select this generic type to define a probe class. Specify the name of the probe class in the ECC queue topic field.
-   [**SNMP Probe**](../concept/c_SNMPProbe.md): Select this probe type for network devices, such as routers.
-   [**WMI Probe**](../reference/r_WMIRunnerProbe.md): Select this probe type for Windows devices.


</td></tr><tr><td>

ECC queue topic

</td><td>

Enter a descriptive term for the function of the probe. The probe uses this label as the **Topic** field for incoming ECC queue messages. The term does not have to be unique. For example, all the UNIX probes might have an ECC queue topic value of **SSHCommand**.By default, probes use the following ECC queue topics:

-   CimProbe
-   Multiprobe
-   Powershell probe
-   SCPRelay
-   SSHCommand
-   SNMP
-   WMIRunner


</td></tr><tr><td>

ECC queue name

</td><td>

Enter either a descriptive name for human use, or the actual command the probe is to run. For example, if the value in the ECC queue topic field is **SSHCommand**, then enter the actual shell command to run in this field.

</td></tr><tr><td>

Cache results

</td><td>

Select this option to cache this probe's results to improve overall discovery performance. The probe results cache should be enabled only for those probes and sensors whose output is unlikely to change. For example, the Linux – CPU sensor is cached because CPU information seldom changes. The cache is turned on by default for base system probes and sensors whose output is unlikely to change.**Warning:** Do not turn on the cache for classification and identification probes. Furthermore, do not turn on the cache for probes that trigger additional probes because this may prevent them from being triggered.

</td></tr><tr><td>

Classic Mode

</td><td>

Select this option to cache this probe's results in the Starting in Fuji, select this option to debug the post-processing script on the ServiceNow instance instead of the MID Server. This mode is only valid if a post-processor script exists. Use the Classic mode to debug post-processing scripts in the test environment. ServiceNow does not recommend use of the Classic mode in the production environment.

</td></tr><tr><td>

Post processor script

</td><td>

Define an optional post-processing script that runs on the MID Server. The script accepts probe results as an input and outputs a JSON string that is sent back to the instance for a sensor to use as input. Use this type of script to accomplish tasks like parsing data.All probe post-processing scripts and their corresponding sensors have access to the following global variables:

-   `current`: Sets the attribute to current. Same functionality that exists in sensors. They are attributes of the device that is discovered.
-   `related_data`: Any additional data to be passed from the probes post-processing scripts, such as `related_list`.
 All probe post-processing scripts and their corresponding sensors have access to the following methods:

-   `log(string)`: Logs the string to the MID Server and the ServiceNow instance log files.
-   `getParameter(param)`: Gets the parameter from the ECC queue payload.


</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

5.  Modify these related lists if necessary.

    |Related list|Description|
    |------------|-----------|
    |Probe Parameters|Parameters that control the functionality of the probe. See [Set probe parameters](t_SetProbeParameters.md) for instructions.|
    |Sensors that react to this probe or Sensors|The sensors that this probe utilizes.|
    |Included by MultiProbe|If this probe is included with other probes as a MultiProbe.|
    |MultiSensor Scripts|Scripts that run for multiple sensors.|
    |Versions|The version of the probe. If the **State** is **Current**, the probe is the most up to date with your version of the instance. If not, you do not have the most current version and you might need to realign it. See [Align versions of customized probes and sensors](t_AlignVerCustProbeSens.md) for instructions.|

6.  Click **Test probe**.

7.  On the Test Probe window, enter the IP address of the target and select the MID Server.

    Only **Up** and **Validated** MID Servers are able to be selected.

8.  Click **OK**.

9.  [Check the ECC Queue](../reference/r_DiscoveryStatusECCQueue.md) for the MID Server to see the results.


## What to do next

Add the probe to the **Triggers Probe** related list on the appropriate classifier. See [Create a Discovery CI classification](create-discovery-ci-classification.md) for a description of the fields and related lists on the classifier form.

**Parent Topic:**[Discovery probe management](../reference/r_Probes.md)

