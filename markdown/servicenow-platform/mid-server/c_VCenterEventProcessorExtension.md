---
title: vCenter event collector
description: The vCenter event collector is a MID Server extension that listens for vCenter-related events and updates the CMDB accordingly.Configure the vCenter event collector extension in the MID Server module, and then add or remove supported events.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# vCenter event collector

The vCenter event collector is a MID Server extension that listens for vCenter-related events and updates the CMDB accordingly.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>The event collector allows the CMDB to be updated with changes to virtual machines \(VMs\), in addition to the updates detected by Discovery. A change to a VM is sent as an event from the vCenter server to the vCenter event collector. When an event is received, the CMDB is updated accordingly. Full vCenter Discovery does not need to rerun. For some events, such as powered on and powered off events, Discovery does not need to run again at all. For most events, Discovery runs only on the necessary vCenter resource.

For example, if a VM is turned off, the vCenter server sends the event `VmPoweredOffEvent`. The vCenter event collector receives and processes the event and the CMDB is updated to reflect that the state of the corresponding VM is set to **off**.

**Important:**

With this extension, Discovery can only modify the state of a VM which exists in the CMDB. When an event with "CreatedEvent" occurs in its name, such as VmCreatedEvent, Discovery scans that VM and then creates the CI using the data it collects. When a new event occurs involving that CI, Discovery can update the existing record without launching another scan.

vCenter event collector supports [domain separation](https://www.servicenow.com/docs/access?context=c_DiscoveryDomainSeparation&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) by inheriting the domain of the specified Mid Server in the event collector context. However, it does not support multi-domain Mid Server configuration.

See [Discovery for VMware vCenter](https://www.servicenow.com/docs/access?context=c_DiscoveryForVMwareVCenter&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for supported versions of vCenter.

## How vCenter events are processed

The MID Server listens for the vCenter events configured in the vCenter Event Collector form. When one of these events is returned from vCenter, the instance parses the payload with a business rule that converts the vCenter event into a system event \(sysevent\). The instance then uses that sysevent to perform tasks, such as email notification.

**Note:** If the MID server is paused when a vCenter event occurs, the MID server still processes the event. In this case, it is possible for the event collector to display a status of **Started**.

The resulting sysevents contain these values:

-   **Name**: Name of the system event created from the vCenter event. This value is always **automation.vcenter**.
-   **Parm1**: vCenter event that was returned. This event must be associated with an event collector record.
-   **Parm2**: Event data provided by vCenter, in JSON format.

![Log entries for vCenter events](../image/vCenterSystemEvents.png "Log entries for vCenter events")

## Supported vCenter events

The following events are the only vCenter events handled by the base system when Discovery is activated. If you have upgraded your instance from an earlier version, you might not have the default events added with later releases. To use the missing events, manually add them.

<table id="table_ejj_rtz_ky"><thead><tr><th>

Event name

</th><th>

Description

</th><th>

Launches probe

</th></tr></thead><tbody><tr><td colspan="3">

**VM events**

</td></tr><tr><td>

VmPoweredOnEvent

</td><td>

The VM has been powered on from the powered off state or resumed from the suspended state. This event is sent when the VM is powered on. It does not account for the time it may take to boot the host operating system.

</td><td>

None

</td></tr><tr><td>

DrsVmPoweredOnEvent

</td><td>

The VM has been powered on by a distributed resource schedule \(DRS\), which balances workload between available resources.

</td><td>

None

</td></tr><tr><td>

VmRestartedOnAlternateHostEvent

</td><td>

The VM was restarted on another host because the original host failed.

</td><td>

None

</td></tr><tr><td>

VmPoweredOffEvent

</td><td>

The VM has been powered off. If the host OS is shut down, this event is sent after the host OS shuts down and the VM enters the powered off state.

</td><td>

None

</td></tr><tr><td>

VmPowerOffOnIsolationEvent

</td><td>

The VM has been powered off on an isolated host in an HA cluster.

</td><td>

None

</td></tr><tr><td>

VmShutdownOnIsolationEvent

</td><td>

The VM has been shut down on an isolated host in an HA cluster.

</td><td>

None

</td></tr><tr><td>

VmSuspendedEvent

</td><td>

The VM is suspended. This event is sent after the VM suspension is complete.

</td><td>

None

</td></tr><tr><td>

VmRelocatedEvent

</td><td>

The VM has been relocated while offline \(either suspended or powered off\). A VM migration of the VM to a different host, or the migration of any storage used by the VM triggers the event. Moves relationships.

</td><td>

None

</td></tr><tr><td>

VmMigratedEvent

</td><td>

One or both of the following occurs:-   The VM has been hot-migrated, with vMotion, to another ESX server.
-   The storage for the VM has been hot migrated.

Only Updates relationship and Deep Discovery.

</td><td>

None

</td></tr><tr><td>

DrsVmMigratedEvent

</td><td>

Migration of a VM recommended by a DRS. Moves relationships.

</td><td>

None

</td></tr><tr><td>

VmRemovedEvent

</td><td>

The VM instance has been deleted from vCenter.

</td><td>

None

</td></tr><tr><td>

VmClonedEvent

</td><td>

The VM was cloned successfully.Creates new records and performs Quick Discovery.

</td><td>

VMWare - vCenter VMs

</td></tr><tr><td>

VmCreatedEvent

</td><td>

The VM was successfully created.Creates new records and performs Quick Discovery.

</td><td>

VMWare - vCenter VMs

</td></tr><tr><td>

VmDeployedEvent

</td><td>

The VM was deployed successfully.Creates new records and performs Quick Discovery.

</td><td>

VMWare - vCenter VMs

</td></tr><tr><td>

VmDiscoveredEvent

</td><td>

The vCenter successfully discovers the VM.Creates new records and performs Quick Discovery.

</td><td>

VMWare - vCenter VMs

</td></tr><tr><td>

VmRegisteredEvent

</td><td>

The VM was successfully registered.Creates new records and performs Quick Discovery.

</td><td>

VMWare - vCenter VMs

</td></tr><tr><td>

VmReconfiguredEvent

</td><td>

The VM was reconfigured.Creates new records and performs Quick Discovery.

</td><td>

VMWare - vCenter VMs

</td></tr><tr><td>

VmInstanceUuidAssignedEvent

</td><td>

A new instance UUID was assigned to the VM. Updates VM instance UUID.

</td><td>

None

</td></tr><tr><td>

VmRenamedEvent

</td><td>

The VM was successfully renamed. Changes the name.

</td><td>

None

</td></tr><tr><td>

VmUuidAssignedEvent

</td><td>

A new BIOS UUID was assigned to the VM. Adds the UUID of the VM.

</td><td>

None

</td></tr><tr><td>

VmMacAssignedEvent

</td><td>

A new MAC address was assigned to the VM. Assigns MAC address to event and triggers VMware-VM nics probe.

</td><td>

VMWare - vCenter VM NICs

</td></tr><tr><td>

VmMacChangedEvent

</td><td>

The MAC address of a VM was changed. Assigns MAC address to event and triggers VMware-VM nics probe.

</td><td>

VMWare - vCenter VM NICs

</td></tr><tr><td>

VmGuestShutdownEvent\*

</td><td>

The guest VM shut-down.

</td><td>

None

</td></tr><tr><td>

VmStoppingEvent

</td><td>

The VM stopped.

</td><td>

None

</td></tr><tr><td>

VmResettingEvent

</td><td>

The VM reset.

</td><td>

None

</td></tr><tr><td colspan="3">

**Cluster events**

</td></tr><tr><td>

ClusterCreatedEvent

</td><td>

A cluster was created.

</td><td>

VMWare - vCenter Clusters

</td></tr><tr><td>

ClusterReconfiguredEvent

</td><td>

A cluster was reconfigured.

</td><td>

VMWare - vCenter Clusters

</td></tr><tr><td>

ClusterDestroyedEvent

</td><td>

A cluster was destroyed.

</td><td>

None

</td></tr><tr><td colspan="3">

**Datastore events**

</td></tr><tr><td>

DatastoreRenamedEvent

</td><td>

A datastore was renamed.

</td><td>

None

</td></tr><tr><td>

VMFSDatastoreCreatedEvent

</td><td>

A VM File System \(VMFS\) datastore was created.

</td><td>

VMWare - vCenter Datastores

</td></tr><tr><td>

DatastoreDiscoveredEvent

</td><td>

A host was added to VirtualCenter and datastores were discovered.

</td><td>

VMWare - vCenter Datastores

</td></tr><tr><td>

NASDatastoreCreatedEvent

</td><td>

An Network Attached Storage \(NAS\) datastore was created.

</td><td>

VMWare - vCenter Datastores

</td></tr><tr><td>

LocalDatastoreCreatedEvent

</td><td>

A local datastore was created.

</td><td>

VMWare - vCenter Datastores

</td></tr><tr><td>

VMFSDatastoreExpandedEvent

</td><td>

A datastore was expanded.

</td><td>

VMWare - vCenter Datastores

</td></tr><tr><td>

DatastoreDestroyedEvent

</td><td>

A datastore was removed from VirtualCenter.

</td><td>

None

</td></tr><tr><td colspan="3">

**Network events**

</td></tr><tr><td>

DVPortgroupCreatedEvent

</td><td>

A port group was created.

</td><td>

VMWare - vCenter Networks

</td></tr><tr><td>

DVPortgroupRenamedEvent

</td><td>

A port group was renamed.

</td><td>

None

</td></tr><tr><td>

DVPortgroupDestroyedEvent

</td><td>

A port group was destroyed.

</td><td>

None

</td></tr><tr><td colspan="3">

**Resourcepool events**

</td></tr><tr><td>

ResourcePoolDestroyedEvent

</td><td>

A resource pool was destroyed.

</td><td>

None

</td></tr><tr><td>

ResourcePoolCreatedEvent

</td><td>

A resource pool was created.

</td><td>

VMWare - vCenter Clusters

</td></tr><tr><td>

ResourcePoolMovedEvent

</td><td>

A resource pool was moved.

</td><td>

VMWare - vCenter Clusters

</td></tr><tr><td>

ResourcePoolReconfiguredEvent

</td><td>

A resource pool was reconfigured.

</td><td>

VMWare - vCenter Clusters

</td></tr><tr><td colspan="3">

**DVS events**

</td></tr><tr><td>

DvsCreatedEvent

</td><td>

A distributed virtual switch was created.

</td><td>

VMWare - vCenter Networks

</td></tr><tr><td>

DvsRenamedEvent

</td><td>

A distributed virtual switch was renamed.

</td><td>

None

</td></tr><tr><td>

DvsDestroyedEvent

</td><td>

A distributed virtual switch was destroyed.

</td><td>

None

</td></tr><tr><td colspan="3">

**Datacenter events**

</td></tr><tr><td>

DatacenterCreatedEvent

</td><td>

A datacenter was created.

</td><td>

VMWare - vCenter Datacenters

</td></tr><tr><td>

DatacenterRenamedEvent

</td><td>

A datacenter was renamed.

</td><td>

None

</td></tr></tbody>
</table>## Configure and run the vCenter event collector extension

Configure the vCenter event collector extension in the MID Server module, and then add or remove supported events.

### Before you begin

Before configuring event collectors, perform these tasks:

-   Deploy and start a MID Server.
-   Ensure that the MID Server has access to the vCenter.
-   Run discovery on the vCenter.

Role required: agent\_admin, admin

### About this task

Multiple MID Servers can listen to the same vCenter instance, and you can add multiple Event Collectors for different vCenters to a single MID Server. Make sure you configure the events on the event collector record that specify the correct MID Server.

**Note:** You can add events to the vCenter event collector. However, not every event is supported by the base system event handlers. If you want to handle events other than those supported in the base Discovery system, you must create a script action to process the events.For instructions, see [Script actions](https://www.servicenow.com/docs/access?context=r_ScriptActions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US). As a reference, the instance processes the vCenter events in the base system with a script action called **Discovery: Process vCenter events**. Do not edit or delete this script action.

To configure the vCenter event processor extension:

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Extensions** &gt; **vCenter Event Collectors**.

2.  Click **New** or open an existing extension.

3.  Fill in the fields, as appropriate from the table.

4.  Right-click in the header bar and click **Save** in the context menu.

    The **vCenter Event** related list appears, containing the default events that the system is configured to handle.

5.  To select a different vCenter event, click **Edit** in the **vCenter Event** related list and browse for the event.

    The slushbucket does not display all the available events in the opening list. Use the filter to browse for events not displayed.

6.  Under **Related Links** click **Start** to save the events in this collection and start the collector.

    The Related Links in this form work as follows:

<table id="table_llg_v1q_g3b"><thead><tr><th>

Related Link

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start

</td><td>

Starts the collector if it is not running. The extension connects to the specified vCenter server by enumerating the VMware credentials in the credential set until a connection can be made. Next, the extension tells the vCenter server to supply the events specified in the Collector Context.

</td></tr><tr><td>

Stop

</td><td>

Stops the running collector on the configured MID Server. No action is taken if the extension is not running.

</td></tr><tr><td>

Restart

</td><td>

Stops, then starts the collector on the configured MID Server.

</td></tr><tr><td>

Test

</td><td>

Tests the parameters for validity. If the IP address, hostname, and the set of events is valid then the test returns a successful status. If any of the parameters are incorrect, an error is shown. Running a test does not affect any extensions that are currently running.

</td></tr><tr><td>

Update parameters

</td><td>

Sends updated parameters to the collector. Any changes you make to the collector while the MID Server is running do not take effect immediately when they are saved. If you click this control when the collector is not running, no update is made.In the case of the vCenter extension, the collector first tests the parameters for validity. If the parameters are valid, the extension disconnects from the vCenter server and reconnects with the new parameters.

</td></tr></tbody>
</table>    ![Event collector](../image/vCenterEventCollector.png)

<table id="table_vfn_tp4_cv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for this vCenter event collector extension for easy identification.

</td></tr><tr><td>

Short description

</td><td>

A description of this collector.

</td></tr><tr><td>

Extension

</td><td>

\[Read-Only\] The collector type is automatically set to **vCenterExtension**.

</td></tr><tr><td>

Status

</td><td>

This field auto-populates with the status of the collector. This field is blank until the collector is started. After issuing a command to the collector, you see one of these values:

 -   **Started**: The collector is running.
-   **Stopped**: The collector is not running.
-   **Offline**: The MID Server is down.
-   **Error**: The collector failed with an error.
 **Note:** The MID Server continues to process vCenter events, even if it is paused. The status of the event collector may show as **Started**.

</td></tr><tr><td>

Error Message

</td><td>

Message describing any error that causes a command, such as **Start** or **Stop**, to fail. This field only appears when the value in the **Status** field is **Error**.

</td></tr><tr><td>

Execute on

</td><td>

Location for running this collection. The possible options are **Specific MID Server** or **Specific MID Server Cluster**.

</td></tr><tr><td>

MID Server

</td><td>

The name of the designated MID Server if you selected **Specific MID Server** in the **Execute on** field. The name of the designated MID Server cluster if you selected **Specific MID Server Cluster**. If you selected the MID Server cluster option, an algorithm determines which server in the cluster runs the collector.

</td></tr><tr><td>

vCenter

</td><td>

The IP address or hostname of the vCenter server.

</td></tr><tr><td>

Executing on

</td><td>

\[Read-Only\] The name of the MID Server on which the collector is running. This field shows the name of the MID Server even if the MID Server is down. If the collector is stopped by the user, this field is empty.

</td></tr></tbody>
</table>
**Related topics**  


[VMware discovery](https://www.servicenow.com/docs/access?context=c_DiscoverVMwareInfrastructure&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

