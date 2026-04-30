---
title: VM instance state and status fields
description: These tables represent the state and status of the cmdb\_ci\_vm\_instance in various flows such as vCenter Discovery and vCenter Events and the Business Rules which are triggered.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-23"
reading_time_minutes: 1
keywords: [Virtual Machine Instance, VM instance, VM state, VM status]
breadcrumb: [VMware, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# VM instance state and status fields

These tables represent the state and status of the cmdb\_ci\_vm\_instance in various flows such as vCenter Discovery and vCenter Events and the Business Rules which are triggered.

<table id="table_dmt_nxx_mxb"><thead><tr><th>

Source

</th><th>

Script or Event name

</th><th>

Field name

</th><th>

VM previous state

</th><th>

VM new state

</th></tr></thead><tbody><tr><td>

vCenter Discovery

</td><td>

VCenterVMsSensor

</td><td>

Install Status

</td><td>

Retired

</td><td>

Installed

</td></tr><tr><td>

vCenter Discovery

</td><td>

VCenterDatacentersSensor

</td><td>

Install Status

 State

 Operational status

</td><td>

Installed

</td><td>

Retired

 Terminated

 Non-operational

</td></tr></tbody>
</table><table id="table_kvr_2zx_mxb"><thead><tr><th>

Source

</th><th>

Script or Event name

</th><th>

Field name

</th><th>

VM previous state

</th><th>

VM new state

</th></tr></thead><tbody><tr><td>

vCenter events

</td><td>

VCenterVmStateUpdater

 powerOnEvtsToUse = \[ 'VmPoweredOffEvent', 'VmPowerOffOnIsolationEvent', 'VmShutdownOnIsolationEvent', 'VmSuspendedEvent' \],

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Installed

 ON

</td></tr><tr><td>

vCenter events

</td><td>

powerOffEvtsToUse = \[ 'VmPoweredOnEvent', 'DrsVmPoweredOnEvent', 'VmRestartedOnAlternateHostEvent', 'VmSuspendedEvent' \],

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Installed

 OFF

</td></tr><tr><td>

vCenter events

</td><td>

suspendEvtsToUse = \[ 'VmPoweredOnEvent', 'DrsVmPoweredOnEvent', 'VmRestartedOnAlternateHostEvent', 'VmPoweredOffEvent', 'VmPowerOffOnIsolationEvent' \]

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Installed

 Paused

</td></tr><tr><td>

vCenter events

</td><td>

VmRemovedEvent

</td><td>

Install Status

 State

</td><td>

Installed

 Any

</td><td>

Retired

 Terminated

</td></tr></tbody>
</table><table id="table_uc2_g1y_mxb"><thead><tr><th>

Business rule

</th><th>

Field name

</th><th>

Plugin name

</th></tr></thead><tbody><tr><td>

Cascade Operational Status to vminstance

</td><td>

cmdb\_ci\_server: Operational status

</td><td>

Pattern Designer

</td></tr><tr><td>

Sync Ops Status for CMDB CI

</td><td>

-   cmdb\_ci: Operational status, Install Status
-   cmdb\_ci\_hardware: Operational status, Hardware Status, Substatus

</td><td>

CMDB

</td></tr></tbody>
</table>**Parent Topic:**[VMware discovery](../concept/c_DiscoverVMwareInfrastructure.md)

**Related topics**  


[Discovery for VMware vCenter](../concept/c_DiscoveryForVMwareVCenter.md)

[ESXi server discovery](r_DiscoverESXServers.md)

[Standalone ESXi discovery](StandaloneESXiDiscovery.md)

[VMware virtual machines](../concept/c_VMwareVirtualMachines.md)

[Datastore Discovery](../concept/c_DatastoreDiscovery.md)

