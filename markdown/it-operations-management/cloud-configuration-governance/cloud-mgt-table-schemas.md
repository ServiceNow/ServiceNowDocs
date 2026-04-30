---
title: Schemas of Cloud Provisioning and Governance tables
description: The tables are cloud-agnostic and can therefore hold data for any cloud provider.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Schemas of Cloud Provisioning and Governance tables

The tables are cloud-agnostic and can therefore hold data for any cloud provider.

## Load balancer table

The load balancer table \[cmdb\_ci\_cloud\_load\_balancer\] extends from \[cmdb\_ci\_vm\_object\], which extends from \[cmdb\_ci\]. Click to enlarge the image.

![Load balancer CMDB object model](../image/schema-load-balancer.png "Schema load balancer")

|Attribute|Description|
|---------|-----------|
|object\_id|Identifier that typically holds the load balancer name as the value.|
|canonical\_hosted\_zone\_id|ID of the Amazon Route 53 hosted zone for the load balancer.|
|canonical\_hosted\_zone\_name|DNS name of the load balancer.|
|dns\_name|Public DNS name of the load balancer.|
|fqdn|DNS name as fully qualified domain name. Can also be a CNAME record pointed to the DNS name.|
|state|State of the load balancer: **available** or **terminated**.|

## Network resource table

The network resource table \[cmdb\_ci\_network\] extends from \[cmdb\_ci\_vcenter\_object\], which extends from \[cmdb\_ci\_vm\_object\], which extends from \[cmdb\_ci\]. Click to enlarge the image.

![Network table object model](../image/schema-network.png "Network table object model")

<table id="table_vvb_tjn_5cb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object\_id

</td><td>

Identifier that typically holds the network ID as the value. Uniquely identifies an object within a cloud.

</td></tr><tr><td>

name

</td><td>

Name of the network.

</td></tr><tr><td>

cidr

</td><td>

IP Address range. Classless inter-domain routing is a set of internet protocol standards that is used to create unique identifiers for networks.

</td></tr><tr><td>

default\_gateway

</td><td>

Holds InternetGatewayID if we attach IntenetGateway to the network.A default gateway serves as an access point or IP router that a networked computer uses to send information to a computer in another network or Internet. The specified gateway is used by default unless an application specifies a different gateway.

</td></tr><tr><td>

Broadcast\_address

</td><td>

IP address used to transmit messages and data packets to network systems.

</td></tr><tr><td>

Is\_shared

</td><td>

Boolean.true: Network shared across other projects.

 false: Network not shared across other projects.

</td></tr><tr><td>

max\_ports

</td><td>

Maximum number of hosts that can be connected to the network

</td></tr><tr><td>

is\_external

</td><td>

Boolean.true: Network is external.

 false: Network is internal.

</td></tr><tr><td>

terminated\_on

</td><td>

Time that the network was de-provisioned.

</td></tr><tr><td>

state

</td><td>

State of the network: **available** or **terminated**.

</td></tr><tr><td>

netmask

</td><td>

Type of CIDR. 32-bit mask that divides an IP address into subnets and specify the hosts that are available on the network.

</td></tr><tr><td>

dhcp\_enabled

</td><td>

Boolean:true: Dynamic IP address is assigned to host

 false: Static IP address is assigned to host

</td></tr></tbody>
</table>## Storage volume resource table

The storage volume resource table \[cmdb\_ci\_storage\_volume\] extends from \[cmdb\_ci\]. Click to enlarge the image.

![Storage volume resource table object model](../image/schema-storage-volume.png "Schema storage volume")

<table id="table_wvb_34n_5cb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object\_id

</td><td>

Identifier that typically holds the object ID as the value. Uniquely identifies an object within a cloud.

</td></tr><tr><td>

volume\_id

</td><td>

Identifier that typically holds the volume ID as the value. Uniquely identifies an object within a cloud.

</td></tr><tr><td>

volume\_container

</td><td>

For NetApp only, LUN becomes the volume and NetApp volume becomes the volume container.

</td></tr><tr><td>

sharable

</td><td>

Boolean.true: Volume is shared by multiple VMs.

 false: Volume is not shared by multiple VMs.

</td></tr><tr><td>

storage\_type

</td><td>

Type of storage.-   AWS: Block
-   Azure: PageBlob
-   vSphere: VMware vdisk

</td></tr><tr><td>

size

</td><td>

Total capacity of the volume.

</td></tr><tr><td>

free\_space

</td><td>

Available space of the volume

</td></tr><tr><td>

state

</td><td>

State of the volume: **available** or **in\_use**.

</td></tr><tr><td>

share\_count

</td><td>

Number of VMs that are shared by the volume.

</td></tr></tbody>
</table>## Virtual server resource table

The virtual server resource table \[cmdb\_ci\_vm\_instance\] extends from \[cmdb\_ci\_vm\_object\], which extends from \[cmdb\_ci\]. Click to enlarge the image.

![Virtual server table object model](../image/schema-virtual-server.png)

<table id="table_wtq_spn_5cb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object\_id

</td><td>

Identifier that typically usually holds the VM instance ID. Uniquely identifies an object within a cloud.

</td></tr><tr><td>

name

</td><td>

Name of the VM.

</td></tr><tr><td>

state

</td><td>

State of the VML: **on**, **off**, or **terminated**.

</td></tr><tr><td>

cpus

</td><td>

Number of CPUs.

</td></tr><tr><td>

memory

</td><td>

Memory size in megabytes.

</td></tr><tr><td>

disks

</td><td>

Number of disk drives.

</td></tr><tr><td>

disk\_size

</td><td>

Total size of disks in gigabytes.

</td></tr><tr><td>

nics

</td><td>

Number of network interface adapters.

</td></tr><tr><td>

terminated\_on

</td><td>

Time that the instance was terminated.

</td></tr><tr><td>

termination\_protection

</td><td>

Boolean. Default value is false.true: Can prevent the instance from being accidentally terminated using Amazon EC2.

 false: Cannot prevent the instance from being accidentally terminated using Amazon EC2.

</td></tr></tbody>
</table>