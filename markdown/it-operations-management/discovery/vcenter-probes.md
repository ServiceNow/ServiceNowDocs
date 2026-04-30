---
title: vCenter probes and probe parameters
description: vCenter probes scan virtual machines using VMware's vSphere product suite. Each probe scans for different kinds of data, such as networks, NICs, and tags. The VMware - vCenter probe that discovered all vCenter objects in previous releases is deprecated in the Istanbul release and replaced by multiple probes.vCenter Discovery extension allows you to collect additional attributes of currently discovered CI types or collect attributes of new CI types by triggering custom probes from an existing sensor.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# vCenter probes and probe parameters

vCenter probes scan virtual machines using VMware's vSphere product suite. Each probe scans for different kinds of data, such as networks, NICs, and tags. The VMware - vCenter probe that discovered all vCenter objects in previous releases is deprecated in the Istanbul release and replaced by multiple probes.

## Upgrade changes

In upgraded systems, the vCenter process classifier and the vmapp port probe are configured to trigger the VMware - vCenter Datacenters probe. This probe then triggers the probes that discover individual vCenter objects such as hosts, storage, and datastores. The legacy probe, VMware - vCenter, is still in the system but is not triggered to run in the updated instance.

## Available vCenter probes and probe parameters

vCenter probe parameters allow you to disable the probes for the objects you are not interested in discovering. You can also reduce the size of the payload of a probe by specifying a page size.

**Important:** Before disabling a probe, be aware of any dependencies the probe might have. If the probe you disable triggers another probe, the dependent probe is also disabled, and cannot collect data.

![Relationship of vCenter elements to probe parameters](../image/vCenterProbeParametersDiagram.png "Relationship of vCenter elements to probe parameters")

These parameters are available for vCenter probes.

**Note:** By default, these parameters are not set in the platform, except where noted.

<table id="table_vcenter_probe_parameters"><thead><tr><th>

Probe

</th><th>

Parameters

</th></tr></thead><tbody><tr><td>

VMWare - vCenter Datacenters

</td><td>

-   datacenter\_only \(Cloud Provisioning and Governance\)
-   debug
-   disable\_vm\_probe
-   disable\_network\_probe
-   disable\_datastore\_probe
-   disable\_cluster\_probe
-   datacenters\_only
-   fixed\_credential\_id \(Cloud Provisioning and Governance\)
-   disable\_vm\_nic\_probe
-   disable\_host\_probe
-   disable\_host\_storage\_probe
-   vcenter\_timeout: default 10000 milliseconds \(10 seconds\).

</td></tr><tr><td>

VMWare - vCenter VMs

</td><td>

-   disable\_vm\_nic\_probe
-   disable\_vm\_nic\_vnics \(set to **false**\)
-   disable\_vm\_nic\_vdisks \(set to **true** for Discovery only and **false** when Cloud Provisioning and Governance is enabled\)
-   disable\_vm\_tags\_probe
-   refresh\_state \(Cloud Provisioning and Governance\)
-   page\_size \(100\)

**Note:** The settings for the vnics and vdisks parameters preserves the default behavior of vCenter Discovery.


</td></tr><tr><td>

VMWare - vCenter VM Tags\*

</td><td>

none

</td></tr><tr><td>

VMWare - vCenter VM NICs

</td><td>

none

</td></tr><tr><td>

VMWare - vCenter Networks

</td><td>

page\_size \(500\)

</td></tr><tr><td>

VMWare - vCenter Datastores

</td><td>

page\_size \(500\)

</td></tr><tr><td>

VMWare - vCenter Clusters

</td><td>

-   disable\_host\_probe
-   disable\_host\_storage\_probe
-   page\_size \(1000\)

</td></tr><tr><td>

VMWare - vCenter ESX Hosts

</td><td>

-   disable\_host\_storage\_probe
-   page\_size \(10\)

</td></tr><tr><td>

VMWare - vCenter ESX Hosts Storage

</td><td>

page\_size \(175\)

</td></tr><tr><td>

VMWare - vCenter ESX Hosts License

</td><td>

none

</td></tr><tr><td>

VMWare - vCenter VM Performance

</td><td>

This probe relies on the statistics intervals configured for the vCenter. By default, the following intervals are available:-   5 minutes \(300 seconds\) – this data is saved for 24 hours.
-   30 minutes \(1800 seconds\) – this data is saved for a week
-   2 hours \(7200 seconds\) – this data is saved for a month
-   24 hours \(86400 seconds\) – this data is saved for a year

 The following properties support this probe:

 -   data\_sampling\_weeks\_frame: The period for which the probe retrieves the data, in weeks.
-   data\_sampling\_minutes: The time lapse between taking the data samples.
-   metrics: The collected metrics \(CPU / memory / network / disk\).

 This probe is used only by Cloud Migration Assessment.

 **Important:** To modify the default values for this probe, coordinate with the administrator responsible for the vCenter management. For more information, see [VMware documentation](https://communities.vmware.com/t5/Storage-Performance/vCenter-Performance-Counters/ta-p/2790328).

</td></tr></tbody>
</table>\*For more information, see [VMware tags](r_VCenterDataCollected-1.md#section_v5k_psr_jhb).

Consider the following when setting these parameters:

-   **Disable**: You disable a probe by setting the parameter in the triggering probe. For example, if you are not interested in discovering storage, set the **disable\_host\_storage\_probe** parameter to **true** in the VMWare - vCenter ESX Hosts probe.
-   **Page size**: Page size parameters control the number of CIs to discover with a single probe. Use this parameter to limit payload size by reducing the number of vCenter elements discovered at a time by any probe. The page size expressed in parentheses is the default in the base system.
-   **Debug**: Set the debug parameter in the VMWare - vCenter Datacenters probe to allow debugging for all the vCenter probes. Debugging returns the raw vCenter data in each probe payload.

**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

## Trigger custom probes with the vCenter Discovery extension

vCenter Discovery extension allows you to collect additional attributes of currently discovered CI types or collect attributes of new CI types by triggering custom probes from an existing sensor.

### Before you begin

Role required: admin

### About this task

vCenter sensor records support triggering custom probes that use conditional scripts for gathering data not typically collected by Discovery or for discovering CI types that you create.

**Important:** The vCenter extension is intended to be used to create a single custom probe that extends existing Discovery functionality. Unless you are a user who is familiar with advanced scripting, do not attempt to configure your new probe/sensor to launch an additional probe.

### Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Sensors**.

2.  Select a vCenter sensor record.

    It is important to trigger a new probe at the correct time. For example, if you want to discover additional information about virtual machines in your network, trigger your probe from the VMWare - vCenter VMs sensor. If you trigger your custom probe from the VMWare - vCenter Datacenters sensor, your new probe and the existing VM probe execute in parallel. This might prevent VM records from being created or updated.

3.  Select the **Triggers probes** related list.

4.  Click **New** to create a new probe to be triggered by this sensor or **Edit** to add an existing probe to the list.

    You can also use an existing probe record as a template for your new probe by opening the record and selecting the **Insert and Stay** option from the context menu.

5.  Click the information icon to the right of the probe name to open the **Conditional Probes Triggered by Sensor** record.

6.  View the script.

    The script passes the **parms** and **data** arguments to the function, using values passed to them from the triggering sensor. The script configures the **parms** object, from which the probe parameters are derived. The script returns **true** to trigger the probe or **false** to cancel it.

    In this example, the VMWare – vCenter Datacenters sensor **parms** are all probe parameters that are supported by the Datacenters probe. The **data** argument is an object containing up to 4 arrays, named **vm**, **datastore**, **network**, and **cluster**.

    ![Conditional Probes Triggered by Sensor record](../image/vCenterConditionalProbes.png "Conditional Probes Triggered by Sensor record")


