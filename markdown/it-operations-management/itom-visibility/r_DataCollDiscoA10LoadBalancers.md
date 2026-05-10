---
title: A10 load balancer discovery
description: Discovery and Service Mapping uses patterns to collect information about A10 load balancers.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# A10 load balancer discovery

Discovery and Service Mapping uses patterns to collect information about A10 load balancers.

**Note:** Probe-to-pattern migration is supported for the New York release and later. See the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477) for more information.

The following patterns support the A10 load balancer discovery:

-   A10 Load Balancer
-   A10 Load Balancer SSH
-   A10

The A10 IP Source NAT \(Network Address Translator\) is an extension of the A10 Load Balancer Pattern. The IP Source NAT Pattern extension discovers IP Source NAT pools. This extension is available on Store from the February 2023 release, Store version 1.0.98.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Credentials**

    Configure [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_SNMPCredentials.md) or \(optionally\) [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md).

-   **Discovery and Service Mapping Patterns application**

    To discover A10 load balancer partitions, deploy Discovery and Service Mapping Patterns application 1.0.98 release from the ServiceNow Store.


## Data collected by Discovery during horizontal discovery

<table id="table_hsy_ql3_cy"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td class="sub-head" colspan="2">

A10 Load Balancer \[cmdb\_ci\_lb\_a10\]

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Serial number of the load balancer.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Load Balancer Interface \[cmdb\_ci\_lb\_interface\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the load balancer interface.

</td></tr><tr><td>

MAC Address \[mac\_address\]

</td><td>

MAC address of the load balancer interface, in the following format: 55:0d:f9:98:3i:ae.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the load balancer interface.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the load balancer pool.

</td></tr><tr><td>

Load balancing method \[load\_balancing\_method\]

</td><td>

The method used by the load balancer.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the pool member.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the pool member host.

</td></tr><tr><td>

Service port \[service\_port\]

</td><td>

Port used by the pool member.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the load balancer pool members.

</td></tr><tr><td>

Pool \[pool\]

</td><td>

Pool member.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Load Balancer Services \[cmdb\_ci\_lb\_service\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the load balancer, in the following format: &lt;LB name&gt;:&lt;LB port&gt;.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the FQDN.

</td></tr><tr><td>

Port \[port\]

</td><td>

Port of the load balancer.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the load balancer service.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the load balancer service.

</td></tr><tr><td>

Pool \[pool\]

</td><td>

Pool member of the load balancer service.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

DNS \[cmdb\_ci\_dns\_name\]

</td></tr><tr><td>

Name \[name\]

</td><td>

DNS name.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

DNS IP address.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

A10 Load Balancer Partition \[cmdb\_ci\_lb\_a10\_partition\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the partition.

</td></tr><tr><td>

Index \[index\]

</td><td>

Partition ID. An admin assigns this ID in the process of creating a partition.

</td></tr><tr><td>

Max Aflex \[max\_aflex\]

</td><td>

Maximum number of aFleX scripts that can belong to the partition.

</td></tr><tr><td>

Admin Count \[admin\_count\]

</td><td>

Number of admins assigned to the partition.

</td></tr><tr><td>

L3V \[l3v\]

</td><td>

Value indicating whether Layer 2/3 virtualization is enabled for the partition.

</td></tr><tr><td class="sub-head" colspan="2">

Network Adapter \[cmdb\_ci\_network\_adapter\]

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the network adapter.

</td></tr><tr><td>

Mac address \[mac\_address\]

</td><td>

MAC address of the network adapter.

</td></tr><tr><td>

Alias \[alias\]

</td><td>

Alias of the network adapter.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the network adapter.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the network adapter.

</td></tr><tr><td>

Netmask \[netmask\]

</td><td>

Netmask of the network adapter.

</td></tr><tr><td>

PrimaryIP \[primaryIP\]

</td><td>

PrimaryIP address of the network adapter.

</td></tr><tr><td class="sub-head" colspan="2">

IP Address \[cmdb\_ci\_ip\_address\]

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address.

</td></tr><tr><td>

Netmask \[netmask\]

</td><td>

Netmask to which the IP address belongs.

</td></tr><tr><td>

Version \[version\]

</td><td>

IP version.

</td></tr><tr><td>

Operational Status \[operational\_status\]

</td><td>

Operational status of the IP address.

</td></tr><tr><td class="sub-head" colspan="2">

SNAT IP Pool \[cmdb\_ci\_snat\_ip\_pool\]

</td></tr><tr><td>

NAT Pool Failed \[nat\_pool\_failed\]

</td><td>

The total misses in the pool.

</td></tr><tr><td>

HA Group \[ha\_group\]

</td><td>

High Availability group number associated with the NAT pool.

</td></tr><tr><td>

NET Mask \[net\_mask\]

</td><td>

Netmask of the NAT pool address range.

</td></tr><tr><td>

NAT Pool Total Free \[nat\_pool\_total\_free\]

</td><td>

The total of free addresses in the pool.

</td></tr><tr><td>

NAT Pool Total Used \[nat\_pool\_total\_usage\]

</td><td>

The total of used addresses in the pool.

</td></tr><tr><td>

NAT Pool Port Usage \[nat\_pool\_total\_used\]

</td><td>

The total port usage in the pool.

</td></tr><tr><td>

NAT Pool End Address \[nat\_pool\_end\_address\]

</td><td>

The IP NAT pool end address \(IPv4 or IPv6\).

</td></tr><tr><td>

NAT Pool Start Address \[nat\_pool\_start\_address\]

</td><td>

The IP NAT pool start address \(IPv4 or IPv6\).

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

A unique identifier for the NAT pool, assigned by the A10 device.

</td></tr><tr><td>

Configuration Item \[cmdb\_ci\]

</td><td>

References the A10 Load Balancer \[cmdb\_ci\_lb\_a10\] table.

</td></tr></tbody>
</table>![A10 load balancer Dependency Views map](../image/A10-components.png "Dependency Views showing A10 load balancer and connected components and applications")

## CI relationships

These relationships are created to support A10 load balancer discovery:

<table id="table_ysf_fpq_f987b"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Router Interface \[dscy\_router\_interface\]

</td><td>

Uses::Used by

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Load Balancer Interface \[cmdb\_ci\_lb\_interface\]

</td><td>

Owns::Owned by

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]

</td><td>

Owns::Owned by

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Load Balancer Services \[cmdb\_ci\_lb\_service\]

</td><td>

Used by::Uses

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Load Balancer Services \[cmdb\_ci\_lb\_service\]

</td><td>

Runs on::Runs

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td><td>

Owns::Owned by

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

DNS Name\[cmdb\_ci\_dns\_name\]

</td><td>

Used by::Uses

</td><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td></tr><tr><td>

Network Adapter \[cmdb\_ci\_network\_adapter\]

</td><td>

Owns::Owned by

</td><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td><td>

Owns::Owned by

</td><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td></tr><tr><td>

A10 Load Balancer \[cmdb\_ci\_lb\_a10\]

</td><td>

Owns::Owned by

</td><td>

Source NAT IP Pool \[cmdb\_ci\_snat\_ip\_pool\]

</td></tr></tbody>
</table>## Data collected by Service Mapping during top-down discovery

Service Mapping discovers the connections between the A10 load balancers and applications in the deployment.

![A10 load balancer application service map](../image/A10LoadBalancerServiceWatchMap.png "A10 load balancer application service map")

**Parent Topic:**[Load balancer discovery](../concept/c_LoadBalancers.md)

