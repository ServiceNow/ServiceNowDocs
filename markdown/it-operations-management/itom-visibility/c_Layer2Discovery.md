---
title: Layer 2 discovery
description: Discovery can detect the physical connections, known as layer 2, between network devices.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Layer 2 discovery

Discovery can detect the physical connections, known as layer 2, between network devices.

## Layer 2 discovery process

Discovery uses multiple probes to gather information about network adapters and their Layer 2 connections. The following diagram shows the probes that Discovery launches for network Discovery, including those used for Layer 2 Discovery.

![Layer 2 probes](../image/Layer2DiscoveryProbesDiagram.png)

For example, if Discovery finds a switch in a network, it triggers the **SNMP - Switch - Vlan** probe and the **SNMP - Network - ARPTable** probe. For every Vlan that Discovery finds, it triggers various switch probes. If a switch has routing capabilities, Discovery triggers the **SNMP - Routing** probe to collect network adapter information in the Network Adapter \[cmdb\_ci\_network\_adapter\] table. If Discovery finds a server, it triggers the appropriate Address Resolution Protocol \(ARP\) probe for that operating system. Discovery also supports the use of patterns, such as the **Network Switch** and **Network Router** patterns, which are available by default in Discovery. See [Network switch and router discovery](../reference/r_DataCollDiscoNWRouteAndSwitch.md) for more information.

During the discovery of a network device, Discovery creates records in the Router Interface \[dscy\_router\_interface\] table and the Switchport \[dscy\_switchport\] table. This information contains network adapter information for that device. For SNMP-enabled devices, Discovery gathers the information from a routing probe during the exploration phase. The Layer 2 protocol cache probe runs next to collect neighbor data from the device.

## Retrieving neighbor data

As Discovery gathers network information from the probes on a device, the SNMP - Layer 2 Protocol Caches identifies device neighbors via CDP and LLDP. This probe updates the Device Neighbors \[discovery\_device\_neighbors\] table, which contains the Layer 2 connections between switches. Sometimes, the neighbors of this device might not yet be known to the instance. The neighbor's interface cannot be resolved to a record until Discovery eventually finds the neighbor's side of the relationship. When Discovery runs on the neighboring device, Discovery completes the information for the neighbor's interface for the original reporting device.

Discovery can retrieve neighbor data from these caches on a network device:

-   [Cisco Discovery Protocol \(CDP\)](https://en.wikipedia.org/wiki/Cisco_Discovery_Protocol): Cache on Cisco devices that contains device neighbor information in the form of a protocol specific neighbor ID. Cisco Discovery Protocol \(CDP\).
-   [Link Layer Discovery Protocol \(LLDP\)](https://en.wikipedia.org/wiki/Link_Layer_Discovery_Protocol): Generic cache that contains device neighbor information in the form of a protocol specific neighbor ID.
-   [Address Resolution Protocol \(ARP\)](https://en.wikipedia.org/wiki/Address_Resolution_Protocol): Cache that contains the IP and MAC addresses of all connecting devices and servers.

## How Layer 2 Discovery works

When device discovery is complete, the system runs the Service Discovery - Device Complete business rule on the Device \[discovery\_device\_history\] table. This business rule uses several strategies, together with information from various tables to create **Connects to:Connected by** relationships in the CMDB. Relationships can be created between:

-   A server and a switch
-   Two switches
-   A device and the port of another device
-   The ports of two devices

In the following example, Discovery found a server running AIX, and was also able to find two IP switches on the network. These relationships were created:

-   A **Connects to** relationship between the AIX Server and the two IP switches A and B.
-   A reference between the AIX server and its own network adapter.
-   A **Connects to** relationship between the adapters on the two IP switches \(not shown in the following image\).
-   A **Connects to** relationship between the network adapter of the AIX server and the switch port of IP switch A \(highlighted in red\). This kind of relationship is created by default.

![Layer 2 relationships](../image/layer2-discovery.png)

To view these relationships, open the dependency view for the server. To view the relationship between the two IP switches, open the dependency view from one of the switches and select the **Physical Network Connections** option for the **Dependency Type** in the map settings.

## Layer 2 connection strategies

Layer 2 Discovery uses the following strategies to create relationships between devices in a network:

-   **PhysicalHostConnectionStrategy**

    This strategy creates a connection between a discovered server, which is not a network device, and a network device. This strategy can only create a Layer 2 connection if there is a single MAC address on the port in the switch's forwarding table. If the port has multiple MAC addresses, Discovery does not create a connection between the server and the switch.

    If the switch's port is identified, Discovery creates a **Connects to::Connected by** relationship between the server adapter and the switch port. Otherwise, Discovery creates a **Connects to::Connected by** relationship between the server adapter and the switch itself.

-   **VMLayer2ConnectionStrategy**

    This strategy creates a connection between a VM and a network device. If the number of exceptional MAC addresses is very low \(less than 3 and less than 15% of all MAC address of the ESX server and its VMs\), Discovery creates a Layer 2 connection.

-   **NetworkDeviceLayer2ConnnectionStrategy**

    This strategy creates a connection between a network device and its neighbors. Discovery creates a Layer 2 connection if there is a single neighbor with a neighbor address, a neighbor interface, or both. If the neighbor's interface exists, Discovery creates a **Connects to::Connected by** relationship between the origin interface and the neighbor's interface. Otherwise, Discovery creates a **Connects to::Connected by** relationship between the origin interface and the switch with the neighbor's address.

-   **SpanningTreeLayer2ConnectionStrategy**

    This strategy creates a connection between a network device and the parent of the network device in the spanning tree.

-   **JavaScriptLayer2ConnectionStrategy**

    This strategy calls a Javascript function with empty implementation. This allows for the creation of an additional strategy.


## Address Resolution Protocol \(ARP\) in Layer 2 discovery

The probes for Address Resolution Protocol \(ARP\) map the IP address of a computer or network device to a MAC address. These probes retrieve the IP address and MAC address for a CI from the Network Infrastructure Item \[dscy\_net\_base\] table. Devices that support SNMP, such as Linux computers and network devices, cache two types of address information:

-   **Static**: Manually added address resolutions.
-   **Dynamic**: Hardware name and IP address pairs added to the cache by previous, successful ARP resolutions.

When the ARP table Discovery completes, the system collects all static and dynamic table entries from devices via SNMP. If a new ARP entry is available, it is added to the Network ARP Table \[discovery\_net\_arp\_table\]. If any previously discovered ARP entries are no longer cached in the device ARP table, the system removes the corresponding records from the CMDB using the reconciliation process.

**Note:** If new ARP entries are created after Discovery runs, they are not discovered until the next Discovery schedule. If ARP entries are removed from the device after Discovery runs, the CMDB ARP table is not updated until Discovery runs again.

Discovery provides these probes for extracting IP and MAC address resolution information:

<table id="table_j52_xw4_tt"><thead><tr><th>

Probe

</th><th>

ECC queue topic

</th><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Linux - Network ARP Tables

</td><td>

SSHCommand

</td><td>

sh $\{file:linux\_arp.sh\}This runs a script file to try the net-tools command \(arp -n\) first. If that fails, it will then try the iproute2 command \(ip neighbor\).

</td><td>

SSH command probe that retrieves the network information from the ARP table on a Linux server.

</td></tr><tr><td>

Solaris - Network ARP Tables

</td><td>

SSHCommand

</td><td>

arp -an

</td><td>

SSH command probe that retrieves the network information from the ARP table on a Solaris server.

</td></tr><tr><td>

Windows - Network ARP Table

</td><td>

Powershell

</td><td>

arp -a

</td><td>

Powershell probe that retrieves the network information from the ARP table on a Windows server.

</td></tr><tr><td>

SNMP - Network - ArpTable

</td><td>

SNMP

</td><td>

TableThe SNMP probe uses this OID first: `iso.org.dod.internet.mgmt.mib-2.ip.ipNetToMediaTable ipNetToMediaPhysAddress,ipNetToMediaNetAddress`.

 If the probe fails to return results, it uses this OID:`iso.org.dod.internet.mgmt.mib-2.ip.ipNetToPhysicalTable ipNetToPhysicalNetAddress,ipNetToPhysicalPhysAddress`.

</td><td>

SNMP probe that collects information from the ARP table on a switch or router.

</td></tr></tbody>
</table>## SNMP switch probes

These probes return bridging information from VLANs connected across network switches, including port selection, forwarding tables, and the use of the spanning tree protocol.

-   **SNMP - Switch - BridgePortTable**

    This probe returns all the ports from a switch that are used to create a bridge between network segments.

<table id="table_f3c_rfq_kr"><tbody><tr><td>

Table

</td><td>

Switch Bridge Port Table \[discovery\_switch\_bridge\_port\_table\] This table is used to map between a port number in the discovery\_switch\_fwd\_table and an interface index.

</td></tr><tr><td>

OID

</td><td>

iso.org.dod.internet.mgmt.mib-2.dot1dBridge.dot1dBase.dot1dBasePortTable dot1dBasePort,dot1dBasePortIfIndex

</td></tr><tr><td>

Fields populated

</td><td>

-   cmdb\_ci
-   port
-   interface\_index


</td></tr></tbody>
</table>-   **SNMP - Switch - SpanningTreeTable**

    This probe returns the active path between any two network nodes bridged by a switch.

<table id="table_q8g_ydz_jgb"><tbody><tr><td>

Table

</td><td>

Switch Spanning Tree Table \[discovery\_switch\_spanning\_tree\_table\]. This table is used to find Layer 2 connections between switches.

</td></tr><tr><td>

OID

</td><td>

iso.org.dod.internet.mgmt.mib-2.dot1dBridge.dot1dStp.dot1dStpPortTable dot1dStpPort,dot1dStpPortState,dot1dStpPortEnable,dot1dStpPortDesignatedRoot,dot1dStpPortDesignatedBridge

</td></tr><tr><td>

Fields populated

</td><td>

-   cmdb\_ci
-   port
-   port\_state
-   port\_enable
-   designated\_root
-   designated\_bridge\_mac


</td></tr></tbody>
</table>-   **SNMP - Switch - ForwardingTable**

    This probe returns information from a switch's forwarding table.

<table id="table_mkj_x3q_kr"><tbody><tr><td>

Table

</td><td>

Switch Forwarding Table \[discovery\_switch\_fwd\_table\] This is the forwarding table for the switches.

</td></tr><tr><td>

OIDs

</td><td>

These OIDs are built as needed by the DiscoveryVlanSwitchProcessor script include.-   **Non-Cisco**:
    -   **Q-BRIDGE MIB**: `oid_spec_list = 'table iso.org.dod.internet.mgmt.mib-2.dot1dBridge.qBridgeMIB.qBridgeMIBObjects.dot1qTp.dot1qTpFdbTable dot1qTpFdbAddress.' + vlanIndex + ',dot1qTpFdbPort.' + vlanIndex + ',dot1qTpFdbStatus.' + vlanIndex;`
    -   **BRIDGE MIB**: oid\_spec\_list = 'table iso.org.dod.internet.mgmt.mib-2.dot1dBridge.dot1dTp.dot1dTpFdbTable dot1dTpFdbAddress,dot1dTpFdbPort,dot1dTpFdbStatus’;
-   **Cisco BRIDGE MIB**: `oid_spec_list = 'table iso.org.dod.internet.mgmt.mib-2.dot1dBridge.dot1dTp.dot1dTpFdbTable dot1dTpFdbAddress,dot1dTpFdbPort,dot1dTpFdbStatus’;`


</td></tr><tr><td>

Additional probe called

</td><td>

The SSH probe `Switch - MAC Table` can be triggered by the DiscoveryVlanSwitchProcessor script include to populate additional Layer 2 data. If you are missing Layer 2 data after you run discovery on multiple VLANs, you should enable the triggering of the `Switch - MAC Table` probe and run discovery again. To do this, add this property to the System Property \[sys\_properties\] table: `glide.discovery.sensors.forwardingtable.ssh`. Set the value of the property to **true**. By default this property is false.

</td></tr><tr><td>

Command

</td><td>

show mac address-table

</td></tr><tr><td>

Fields populated

</td><td>

-   cmdb\_ci
-   vlan\_id
-   port
-   status
-   mac\_address \(from the **cmdb\_ci** field in the Network Infrastructure Item \[discovery\_net\_base\] table\)


</td></tr></tbody>
</table>-   **SNMP - Switch - Vlan**

    This probe returns VLAN IDs from a network switch and these OIDs:

    ```
    
    iso.org.dod.internet.private.enterprises.cisco.ciscoMgmt.ciscoVtpMIB.vtpMIBObjects.vlanInfo.vtpVlanTable vtpVlanState
    
    iso.org.dod.internet.private.enterprises.cisco.ciscoMgmt.ciscoVlanMembershipMIB.ciscoVlanMembershipMIBObjects.vmMembership.vmMembershipSummaryTable vmMembershipSummaryVlanIndex,vmMembershipSummaryMemberPorts,vmMembershipSummaryMember2kPorts
    
    iso.org.dod.internet.private.enterprises.juniperMIB.jnxMibs.jnxExMibRoot.jnxExSwitching.jnxExVlan.jnxVlanMIBObjects.jnxExVlanTable jnxExVlanTag
    
    iso.org.dod.internet.mgmt.mib-2.system.sysDescr
    ```

    Other switch types are not supported.


## Port tables

These port tables are populated during horizontal Discovery of a device:

-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Switchport \[dscy\_switchport\]
-   Router Interface \[dscy\_router\_interface\]
-   Load Balancer Interface \[cmdb\_ci\_lb\_interface\]

**Parent Topic:**[Network device discovery](c_NetworkDevices.md)

