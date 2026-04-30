---
title: Network switch and router discovery
description: Discovery identifies and classifies information about network switches and routers.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Network switch and router discovery

Discovery identifies and classifies information about network switches and routers.

Network switches and routers often have very similar capabilities. It is very common for some switches known as Layer 3 switches to have IP routing. Larger routers with optional modules might accept switching modules. Because of these overlaps and the resulting ambiguity of a particular device's classification, Discovery collects the same data for both routers and switches, if it is available in any given device. For details on how Discovery collects data about connections between network devices and other components, see [Layer 2 discovery](../concept/c_Layer2Discovery.md#).

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Prerequisites

-   The router or switch needs to have IP Address information.
-   The system property glide.discovery.L3\_mapping is set to true to discover routers and switches.
-   The router or Layer 3 switch that provides the IP Address needs to have been successfully discovered with populated Exit Interface Routing Rules.
-   If you must populate the \[discovery\_device\_neighbors\] table during horizontal layer 2 discovery of the bgp-enabled devices, set the **BGP router exploration disable** property to **No**. Notice that enabling this property can cause performance issues including out-of-memory issues on the MID Server.

## System properties

You can configure many aspects of Discovery to work according to your personal preferences. The following properties apply to network routers and switches. To view the properties, navigate to **Discovery Definition** &gt; **Properties** unless indicated otherwise.

<table id="table_xdy_vfj_ks"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.L3\_mapping

</td><td>

This creates IP Connecton::IP Connection relation between servers and network devices.-   **Type:** string
-   **Default value:** true
-   **Location:** System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.discovery.max\_concurrent\_invocations\_per\_schedule

</td><td>

Sets a maximum number of scheduled invocations of the same Discovery schedule. It prevents a backlog of scheduled runs if Discovery does not finish before the next invocation is scheduled to run. The value is an integer that represents the max number of automated invocations of the same schedule that may proceed at one time. If the limit has been reached, subsequent scheduled invocations are canceled. A value of 0 or any negative number disables this property. -   **Type:** integer
-   **Default value:** 3
-   **Location:** **Discovery Definition** &gt; **Properties**

**Note:** This property does not apply to schedules that have a 'Run after' configuration set to 'Even if canceled'.

</td></tr></tbody>
</table>For a list of properties used in discovery in general, see [Discovery properties](r_DiscoveryProperties.md).

## Credentials

Discovery explores many kinds of devices, such as switches, routers, and printers, using the SNMP protocol. SNMP Community Credentials do not include a user name, just a password, which is the community string. The default read-only community string for many SNMP devices is public, and Discovery will try that automatically. SNMPv3 credentials require a user name and a key, depending on the protocol selected. Enter the appropriate [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) if they differ from the public community string.

**Note:** SSH is not supported for routers and switches, but is supported for [load balancers](../concept/c_LoadBalancers.md).

## Classifier, pattern, and probes

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifiers

</th><th>

Trigger probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Standard Network RouterStandard Network Switch

</td><td>

-   Horizontal Pattern: launches patterns
-   SNMP-Routing^
-   DNS\*
-   SNMP-Identity\*
-   SNMP-Switch-Vlan\*
-   SNMP-Switching\*
-   SNMP - Network - ArpTable\* \(Standard Network Switch only\)

</td><td>

[Network Router](../../service-mapping/reference/network-router-patterns.md)[Network Switch](../../service-mapping/reference/network-switch-patterns.md)

</td></tr></tbody>
</table>\*For new instances, these probes are inactive on the classifier. Discovery uses patterns for discovery.

^This probe remains active by default for the Standard Network Router classifier, even when Discovery uses pattern discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Discovering stacked switches

The Network Switch shared library supports Cisco stacked switches. The CI table for this is IP Switch \[cmdb\_ci\_ip\_switch\]. Multiple switches in the stack are identified by the primary IP address. Each member of the stack is identified by a combination of elements, including the primary IP address, a name associated with the switch, and the stack mode. The relationship is created between a primary and all of the secondaries. The primary switch has all the fields listed in the table below. The secondary switch has name, serial\_number, model\_id, manufacturer, stack, and stack\_mode.

**Note:** If all the ports on a switch are open for port 161, that switch will have multiple IPs \(one for each port\) but the serial number for all the ports is the same. The CI identification is performed based on the serial number, therefore the same record is updated every time instead of creating a new record.

## Router and switch data

<table id="table_mmn_fhb_2gb"><thead><tr><th>

Table name

</th><th>

Label/Field name

</th><th>

Source

</th></tr></thead><tbody><tr><td>

cmdb\_ci

</td><td>

Serial Number

 serial\_number

</td><td>

SNMP, various MIBs

</td></tr><tr><td>

cmdb\_ci

</td><td>

Manufacturer

 manufacturer

</td><td>

SNMP, RFC1213 MIB

</td></tr><tr><td>

cmdb\_ci

</td><td>

Model ID

 model id

</td><td>

SNMP, RFC1213 MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Name

 name

</td><td>

 

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Model ID

 model ID

</td><td>

SNMP, RFC1213 MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Manufacturer

 manufacturer

</td><td>

SNMP, RFC1213 MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Serial Number

 serial\_number

</td><td>

SNMP, various MIBs

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

IP Address

 ip\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Description

 short\_description

</td><td>

 

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Can route IP

 can\_route

</td><td>

SNMP, IP MIB, BGP MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Can switch IP

 can\_switch

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_router

</td><td>

Port

 port

</td><td>

 

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Name

 name

</td><td>

 

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Model ID

 model ID

</td><td>

SNMP, RFC1213 MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Manufacturer

 manufacturer

</td><td>

SNMP, RFC1213 MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Serial Number

 serial\_number

</td><td>

SNMP, various MIBs

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

IP Address

 ip\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Description

 short\_description

</td><td>

 

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Can route IP

 can\_route

</td><td>

SNMP, IP MIB, BGP MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Ports

 ports

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Can switch IP

 can\_switch

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Can partition VLANs

 can\_partitionvlans

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Stack

 stack

</td><td>

SNMP, entPhysicalTable

</td></tr><tr><td>

cmdb\_ci\_ip\_switch

</td><td>

Stack Mode

 stack\_mode

</td><td>

SNMP, entPhysicalTable

</td></tr><tr><td>

cmdb\_ci\_netgear

</td><td>

Can route IP

 can\_route

</td><td>

SNMP, IP MIB, BGP MIB

</td></tr><tr><td>

cmdb\_ci\_netgear

</td><td>

Can switch IP

 can\_switch

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

cmdb\_ci\_netgear

</td><td>

Can partition VLANs

 cdscy\_router\_interface

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

cmdb\_ci\_netgear

</td><td>

Can Hub

 can\_hub

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

cmdb\_ci\_network\_adapter

</td><td>

IP Address

 ip\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

cmdb\_ci\_network\_adapter

</td><td>

MAC Address

 mac\_address

</td><td>

SNMP, IF MIB

</td></tr><tr><td>

discovery\_device\_neighbors

</td><td>

Neighbor Address

 neighbor\_address

</td><td>

ciscoCdpMIB

</td></tr><tr><td>

discovery\_device\_neighbors

</td><td>

Neighbor ID

 neighbor\_ID

</td><td>

ciscoCdpMIB, lldpMIB

</td></tr><tr><td>

discovery\_device\_neighbors

</td><td>

Neighbor Interface

 neighbor\_interface

</td><td>

ciscoCdpMIB, lldpMIB

</td></tr><tr><td>

discovery\_device\_neighbors

</td><td>

Neighbor Source

 neighbor\_source

</td><td>

ciscoCdpMIB, lldpMIB

</td></tr><tr><td>

discovery\_device\_neighbors

</td><td>

Origin Interface

 origin\_interface

</td><td>

ciscoCdpMIB, lldpMIB

</td></tr><tr><td>

discovery\_net\_arp\_table

</td><td>

IP Address

 IP\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

discovery\_net\_arp\_table

</td><td>

MAC Address

 mac\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

discovery\_switch\_bridge\_port\_table

</td><td>

Interface Index

 interface\_index

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_bridge\_port\_table

</td><td>

Port

 port

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_fwd\_table

</td><td>

MAC Address

 mac\_address

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_fwd\_table

</td><td>

Port

 port

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_fwd\_table

</td><td>

Status

 status

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_fwd\_table

</td><td>

VLAN ID

 vlan\_id

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_spanning\_tree\_table

</td><td>

Designated Bridge MAC

 designated\_bridge\_mac

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_spanning\_tree\_table

</td><td>

Designated Root

 designated\_root

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_spanning\_tree\_table

</td><td>

Port

 port

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_spanning\_tree\_table

</td><td>

Port Enable

 port\_enable

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

discovery\_switch\_spanning\_tree\_table

</td><td>

Port State

 port\_state

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_router\_interface

</td><td>

Name

 name

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_router\_interface

</td><td>

Type

 type

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_router\_interface

</td><td>

Number

 number

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_router\_interface

</td><td>

IP Address

 ip\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_router\_interface

</td><td>

MAC Address

 mac\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_route\_interface

</td><td>

Destination Network

 dest\_ip\_network

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_route\_interface

</td><td>

Type

 type

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_route\_next\_hop

</td><td>

Destination Network

 dest\_ip\_network

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_route\_next\_hop

</td><td>

Type

 type

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_route\_next\_hop

</td><td>

Next Hop

 next\_hop\_ip\_address

</td><td>

SNMP, IP MIB

</td></tr><tr><td>

dscy\_switchport

</td><td>

Type

 type

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_switchport

</td><td>

Status

 status

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_switchport

</td><td>

MAC Address

 mac\_address

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_switchport

</td><td>

Port Number

 port\_number

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_switchport

</td><td>

Interface Name

 interface\_name

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_switchport

</td><td>

Interface Number

 interface\_number

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_fwd\_rule

</td><td>

MAC Address

 mac\_address

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_fwd\_rule

</td><td>

MAC Manufacturer

 mac\_mfr

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_fwd\_rule

</td><td>

Status

 status

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_fwd\_rule

</td><td>

IP address

 ip\_address

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_fwd\_rule

</td><td>

Netmask

 netmask

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Base IP Address

 base\_ip\_address

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Base MAC Address

 base\_mac\_address

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Base Netmask

 base\_netmask

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Type

 type

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Transparent

 transparent

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Source Route

 sourceroute

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Name

 name

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Status

 status

</td><td>

SNMP, dot1dBridge MIB

</td></tr><tr><td>

dscy\_swtch\_partition

</td><td>

Interface Number

 interface\_number

</td><td>

SNMP, dot1dBridge MIB

</td></tr></tbody>
</table>-   **[Turn off collection of port data for SNMP network devices](../task/t_TurnOffCollectionOfPortData.md)**  
In some environments you may not want to collect the port data for SNMP network devices.

**Parent Topic:**[Network device discovery](../concept/c_NetworkDevices.md)

