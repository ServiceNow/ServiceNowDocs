---
title: Citrix NetScaler load balancer discovery
description: Discovery and Service Mapping find Citrix NetScaler load balancers including Server Load Balancing \(GSLB\).
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Citrix NetScaler load balancer discovery

Discovery and Service Mapping find Citrix NetScaler load balancers including Server Load Balancing \(GSLB\).

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Requirements and support

**Important:** Discovery treats load balancers as licensable entities and attempts to discover them primarily using SNMP. If a load balancer in your system, running on a Linux host, has SNMP and SSH ports open, Discovery might classify it based on the SSH port. This classification has priority over SNMP. To ensure that Discovery properly classifies your hardware load balancers, create a Discovery behavior for load balancers that includes SNMP but not SSH. Software load balancers are treated as applications.

Virtual NetScaler load balancers are not fully supported. Discovery supports local server load balancers and GSLB.

## Credentials

-   Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

    **Note:** You also have the option of using [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). However, if the payload size of the data that is returned to the instance is large, the discovery process can fail. In this case, use SNMP credentials instead.

-   \(Optional\) Provide a user with the read access to the **NS.conf** configuration file if you do not want to provide SNMP or SSH credentials.
-   Use [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials for discovery via REST.

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Classifier, pattern, and probes

<table id="table_bfh_4ks_rz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Patterns

</th></tr></thead><tbody><tr><td>

NetScaler Load Balancer

</td><td>

-   Horizontal discovery probe: launches patterns \(see the Patterns column\)
-   NetScaler - Network Path Information \(multiprobe\)
    -   NetScaler - ARP Information
    -   NetScaler - Route Information
-   SNMP - NetScaler - Identity
-   SNMP - NetScaler - Identity - Serial
-   SNMP - NetScaler - Identity Info
-   SNMP - NetScaler - System

</td><td>

-   NetScaler Load Balancer
-   NetScaler Load Balancer NS.CONF
-   NetScaler Load Balancer SSH
-   Netscaler Loadbalancer NITRO

</td></tr></tbody>
</table>To use probes for the horizontal discovery, make sure that the **NetScaler - Network Path Information** multiprobe is active on the **Trigger probes** related list for the **NetScaler Load Balancer** classifier. Then deactivate or remove the **Horizontal discovery** probe from the **Trigger probes** related list.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

**Note:** When using probes and sensors and the system properties**glide.discovery.hostname.snmp\_trusted** and/or **glide.discovery.hostname.dns\_nbt\_trusted** are set to false, the system uses **dns\_name** as the load balancer name. When using the Netscaler Load Balancer pattern, the system currently doesn’t recognize these system properties when they are set to false.

## Connections discovered by Service Mapping during the top-down discovery

Service Mapping performs the top-down discovery of the NetScaler Global Server Load Balancer in the context of application services. It discovers configured URLs of the NetScaler Global Server Load Balancer.

## Data collected by Discovery during horizontal discovery

|Table and field|Description|
|---------------|-----------|
|DNS name \[cmdb\_ci\_dns\_name\]|
|Name \[name\]|The name or the DNS name alias of the NetScaler Global Server Load Balancing \(GSLB\).|
|IP address \[ip\_addresses\]|Management IP address of the NetScaler Global Server Load Balancing \(GSLB\).|
|Port \[port\]|The DNS port that Global Server Load Balancer listens to.|
|Citrix NetScaler `[cmdb_ci_lb_netscaler]`|
|Serial Number \[serial\_number\]|The serial number of the NetScaler device and its current operational status.|
|Operational Status \[operational\_status\]|
|Load Balancer Pool `[cmdb_ci_lb_pool]`|
|Name \[name\]|The name of the pool and the method of load balancing it enables.|
|Load Balancing Method \[load\_balancing\_method\]|
|Load Balancer Pool Member `[cmdb_ci_lb_pool_member]`|
|Name \[name\]|The name, IP address and service port that each pool member uses.|
|IP Address \[ip\_address\]|
|Service Port \[service\_port\]|
|Load Balancer VLAN `[cmdb_ci_lb_vlan]`|
|Name \[name\]|The name of the VLAN and the tag that is associated with this VLAN to identify it.|
|Tag \[tag\]|
|Load Balancer Services `[cmdb_ci_lb_service]`|
|Name \[name\]|Details about the service running on the load balancer, including|
|IP Address \[ip\_address\]|
|Port \[port\]|
|Operational Status \[operational\_status\]|
|Install Status \[install\_status\]|
|Hit count \[hit\_count\]|
|Exit Interface Routing Rules `[dscy_route_interface]`|
|Router Interface \[router\_interface\]|Details about the routing rules for the exit interface, including the interface on the router that ...|
|Configuration item \[cmdb\_ci\]|
|Destination IP network \[dest\_ip\_network\]|
|Next Hop Routing Rules `[dscy_route_next_hop]`|
|Next hop IP address \[router\_interface\]|Details about the routing rules on the load balancer, including the IP addresses of the next hop router on the network. The Configuration item field is the router which is the next hop device.|
|Router Interface \[router\_interface\]|
|Configuration item \[cmdb\_ci\]|
|Destination IP network \[dest\_ip\_network\]|

<table id="table_dcm_kc3_zyb"><tbody><tr><td>

Column name

</td><td>

Type

</td><td>

Reference

</td></tr><tr><td>

ip\_address

</td><td>

IP Address \(Validated IPV4, IPV6\)

</td><td>

 

</td></tr><tr><td>

name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

operational\_status

</td><td>

Integer

</td><td>

 

</td></tr><tr><td>

serial\_number

</td><td>

String

</td><td>

 

</td></tr></tbody>
</table>Data collected during Netscaler Loadbalancer NITRO.

<table id="table_ecm_kc3_zyb"><tbody><tr><td>

Column label

</td><td>

Column name

</td><td>

Type

</td><td>

Reference

</td></tr><tr><td>

Configuration Item

</td><td>

cmdb\_ci

</td><td>

Reference

</td><td>

Configuration Item \(Load Balancer\)

</td></tr><tr><td>

Serial Number

</td><td>

serial\_number

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Serial Number Type

</td><td>

serial\_number\_type

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Valid

</td><td>

valid

</td><td>

True/False

</td><td>

 

</td></tr></tbody>
</table><table id="table_fcm_kc3_zyb"><tbody><tr><td>

Column label

</td><td>

Column name

</td><td>

Type

</td><td>

Reference

</td></tr><tr><td>

Load balancer

</td><td>

load\_balancer

</td><td>

Reference

</td><td>

Configuration Item \(Load Balancer\)

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Tag

</td><td>

tag

</td><td>

Integer

</td><td>

 

</td></tr></tbody>
</table><table id="table_gcm_kc3_zyb"><tbody><tr><td>

Column label

</td><td>

Column name

</td><td>

Type

</td><td>

Reference

</td></tr><tr><td>

Load balancer

</td><td>

load\_balancer

</td><td>

Reference

</td><td>

Configuration Item \(Load Balancer\)

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Operational status

</td><td>

operational\_status

</td><td>

Integer

</td><td>

 

</td></tr><tr><td>

MAC Address

</td><td>

mac\_address

</td><td>

String

</td><td>

 

</td></tr></tbody>
</table><table id="table_hcm_kc3_zyb"><tbody><tr><td>

Column label

</td><td>

Column name

</td><td>

Type

</td><td>

Reference

</td></tr><tr><td>

IP Address

</td><td>

ip\_address

</td><td>

IP Address \(Validated IPV4, IPV6\)

</td><td>

 

</td></tr><tr><td>

Load balancer

</td><td>

load\_balancer

</td><td>

Reference

</td><td>

Configuration Item \(Load Balancer\)

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Port

</td><td>

port

</td><td>

Integer

</td><td>

 

</td></tr></tbody>
</table><table id="table_icm_kc3_zyb"><tbody><tr><td>

Column label

</td><td>

Column name

</td><td>

Type

</td><td>

Reference

</td></tr><tr><td>

Load balancer

</td><td>

load\_balancer

</td><td>

Reference

</td><td>

Configuration Item \(Load Balancer\)

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

String

</td><td>

 

</td></tr></tbody>
</table><table id="table_jcm_kc3_zyb"><tbody><tr><td>

Column label

</td><td>

Column name

</td><td>

Type

</td><td>

Reference

</td></tr><tr><td>

IP Address

</td><td>

ip\_address

</td><td>

IP Address \(Validated IPV4, IPV6\)

</td><td>

 

</td></tr><tr><td>

Load balancer

</td><td>

load\_balancer

</td><td>

Reference

</td><td>

Configuration Item \(Load Balancer\)

</td></tr><tr><td>

Name

</td><td>

name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Pool

</td><td>

pool

</td><td>

Reference

</td><td>

Load Balancer Pool

</td></tr><tr><td>

Service port

</td><td>

service\_port

</td><td>

Integer

</td><td>

 

</td></tr></tbody>
</table>To see the DNS names and alases for a NetScaler load balancer, you must configure the form and add the **DNS Names for CIs** related list. DNS names also include aliases.

**Note:** Discovery populates load balancer interface information that is necessary to map the [network path](../../service-mapping/task/t_CheckNtwrkStrgPath.md) in Service Mapping.

## Configuration item \(CI\) Relationships

These relationships are created to support NetScaler Global Server Load Balancer discovery:

<table id="table_bhf_jis2_ycb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

DNS name \[cmdb\_ci\_dns\_name\]

</td><td>

Uses:Used by

</td><td>

IP address\[cmdb\_ci\_ip\_addresses\]

</td></tr></tbody>
</table>These relationships are created to support NetScaler Loadbalancer NITRO:

<table id="table_syt_bc3_zyb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Netscaler \[cmdb\_ci\_lb\_netscaler\]

</td><td>

Owns::Owned by

</td><td>

interfaces\[cmdb\_ci\_lb\_interface\]

</td></tr><tr><td>

Netscaler \[cmdb\_ci\_lb\_netscaler\]

</td><td>

Owns::Owned by

</td><td>

vlan\[cmdb\_ci\_lb\_vlan\]

</td></tr><tr><td>

Netscaler \[cmdb\_ci\_lb\_netscaler\]

</td><td>

Owns::Owned by

</td><td>

service groups\[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

service groups\[cmdb\_ci\_lb\_pool\]

</td><td>

Owns::Owned by

</td><td>

lbvservers\[cmdb\_ci\_lb\_pool\_member\]

</td></tr><tr><td>

services \[cmdb\_ci\_lb\_service\]

</td><td>

Runs on::Runs

</td><td>

Netscaler \[cmdb\_ci\_lb\_netscaler\]

</td></tr></tbody>
</table>## NetScaler device sysName

To verify the NetScaler device sysName, check the snmp mib and verify the sysName value by running the command: `show snmp mib`.

To change the value of the sysName, run the command: `set mib -name <DNS_NAME or NAME_OF_THE_NETSCALER_LB>` to set the name of the SNMP MIB.

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

