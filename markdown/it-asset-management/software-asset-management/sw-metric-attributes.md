---
title: Software model metric attributes
description: Software model metric attributes and related list field descriptions.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Software model metric attributes

Software model metric attributes and related list field descriptions.

## Metric attributes

<table id="table_bf2_wnn_vzb"><thead><tr><th>

Attribute

</th><th>

Attribute value

</th><th>

Attribute value is unlimited

</th><th>

Description

</th><th>

License metric

</th><th>

Metric group

</th></tr></thead><tbody><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The number of installs each right can license.

</td><td>

Per Named Device

</td><td>

Common

</td></tr><tr><td>

Minimum cores per processor

</td><td>

8

</td><td>

False

</td><td>

The number of core rights that must be applied to a physical processor or set of vCores.

 `Licensable cores = Processors * Max (Minimum cores per processor, Cores)`

</td><td>

Per Core \(with CAL\)

</td><td>

Microsoft

</td></tr><tr><td>

Minimum cores per VM

</td><td>

8

</td><td>

False

</td><td>

The number of core rights that must be applied to a virtual machine \(VM\).

</td><td>

Per Core \(with CAL\)

</td><td>

Microsoft

</td></tr><tr><td>

Maximum active OSEs per server

</td><td>

2

</td><td>

False

</td><td>

The maximum number of Operating System Environments \(OSEs\) allowed to run software on a physical server.

 `Licenses required = (Licensable OSEs/Maximum active OSEs per server) * Licensable cores`

</td><td>

Per Core \(with CAL\)

</td><td>

Microsoft

</td></tr><tr><td>

Minimum cores per server

</td><td>

16

</td><td>

False

</td><td>

The number of core rights that must be applied to a physical server.

 `Licensable cores = Max (Processors * Max (Minimum cores per processor, Cores), Minimum cores per server)`

</td><td>

Per Core \(with CAL\)

</td><td>

Microsoft

</td></tr><tr><td>

Maximum installs per OSE

</td><td>

1

</td><td>

False

</td><td>

The maximum number of installs allowed within one of a server's OSEs.

 `Licenses required = (Licensable installs per OSE/Maximum installs per OSE) * Licensable cores`

</td><td>

Per Core \(with CAL\)

</td><td>

Microsoft

</td></tr><tr><td>

Minimum cores per processor

</td><td>

1

</td><td>

False

</td><td>

The number of core rights that must be applied to a physical processor.

</td><td>

Per Core

</td><td>

Common

</td></tr><tr><td>

Maximum size of instance on cloud

</td><td>

8

</td><td>

False

</td><td>

Oracle Database Standard Edition, Oracle Database Standard Edition One and Oracle Database Standard Edition 2 have maximum limits on the size of the instances to which they’re deployed on Oracle Authorized Cloud Environments such as Microsoft Azure and AWS. Oracle Database Enterprise Edition doesn’t have any maximum limits on the size of the instances to which it’s deployed to on Oracle Authorized Cloud Environments such as Microsoft Azure and AWS.

</td><td>

Per Processor

</td><td>

Oracle

</td></tr><tr><td>

Maximum number of sockets per server

</td><td>

2

</td><td>

False

</td><td>

Oracle Database Standard Edition, Oracle Database Standard Edition One and Oracle Database Standard Edition 2 may only be licensed on servers that have a value less than the maximum number of sockets.

</td><td>

Per Processor

</td><td>

Oracle

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Named User

</td><td>

VMware

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Named User

</td><td>

IBM

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Named User

</td><td>

Common

</td></tr><tr><td>

Maximum VMs per right

</td><td>

2

</td><td>

False

</td><td>

For RHEL Server, this is the number of VMs running on a physical host that each subscription can license. A single VM running on a host needs one subscription.

 For RHEL for Virtual Datacenters, this is the number of VMs that can be licensed with one subscription for each socket-pair on the physical host.

</td><td>

Per Socket-pair

</td><td>

Red Hat

</td></tr><tr><td>

Maximum sockets per right

</td><td>

2

</td><td>

False

</td><td>

The number of sockets on the physical host each subscription can license. A single socket host needs one subscription.

</td><td>

Per Socket-pair

</td><td>

Red Hat

</td></tr><tr><td>

Maximum processors per right

</td><td>

2

</td><td>

False

</td><td>

The maximum number of physical processors each right can license.

 `Licenses required = Processors/Maximum processors per right`

</td><td>

Per Processor

</td><td>

Microsoft

</td></tr><tr><td>

Maximum active OSEs per server

</td><td>

2

</td><td>

False

</td><td>

The maximum number of OSEs allowed to run software on a physical server.

 `Licenses required = Licensable OSEs/Maximum active OSEs per server`

</td><td>

Per Processor

</td><td>

Microsoft

</td></tr><tr><td>

Maximum installs per OSE

</td><td>

1

</td><td>

False

</td><td>

The maximum number of installs allowed within one of the server's OSEs.

 `Licenses required = Licensable installs per OSE/Maximum installs per OSE`

</td><td>

Per Processor

</td><td>

Microsoft

</td></tr><tr><td>

Maximum installs per OSE

</td><td>

1

</td><td>

False

</td><td>

The maximum number of installs allowed within one of the server's OSEs.

 `Licenses required = Licensable installs per OSE`

</td><td>

Server \(Per Instance\)

</td><td>

Microsoft

</td></tr><tr><td>

Maximum installs per right

</td><td>

1

</td><td>

False

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Application Instance

</td><td>

VMware

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per OSI

</td><td>

VMware

</td></tr><tr><td>

Minimum NUPs

</td><td>

5

</td><td>

False

</td><td>

If licensed by Named User Plus \(NUP\), then both Oracle Database Standard Edition and Oracle Database Standard Edition One require a minimum of five NUP licenses each.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Minimum NUPs for WebLogic on-premise deployments

</td><td>

10

</td><td>

False

</td><td>

The minimum number of users required to be licensed for programs accessing a processor. This attribute is used for reconciling entitlements with an Oracle NUP license metric for Oracle WebLogic Standard and WebLogic Enterprise deployed on-premise. For WebLogic Standard, the attribute counts occupied sockets and for WebLogic Enterprise, the attribute counts processor cores.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Maximum number of sockets per server

</td><td>

2

</td><td>

False

</td><td>

Oracle Database Standard Edition, Oracle Database Standard Edition One and Oracle Database Standard Edition 2 may only be licensed on servers that have a value less than the maximum number of sockets.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Minimum users per processor

</td><td>

25

</td><td>

False

</td><td>

The minimum number of users allowed to access a physical processor. This metric attribute is applicable for both on-premise and Oracle Authorized Cloud Environments such as Microsoft Azure and AWS.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Minimum NUPs on cloud

</td><td>

10

</td><td>

False

</td><td>

If licensed by NUP, Oracle Database Standard Edition 2 requires a minimum of 10 NUP licenses per 8 vCPUs on Oracle Authorized Cloud Environments such as Microsoft Azure and AWS.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Maximum size of instance on cloud

</td><td>

8

</td><td>

False

</td><td>

Oracle Database Standard Edition, Oracle Database Standard Edition One and Oracle Database Standard Edition 2 have maximum limits on the size of the instances to which they’re deployed on Oracle Authorized Cloud Environments such as Microsoft Azure and AWS. Oracle Database Enterprise Edition doesn’t have any maximum limits on the size of the instances to which it’s deployed to on Oracle Authorized Cloud Environments such as Microsoft Azure and AWS.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Minimum NUPs for WebLogic cloud deployments

</td><td>

10

</td><td>

False

</td><td>

The minimum number of users required to be licensed for programs accessing a vCPU. This attribute is used for reconciling entitlements with an Oracle NUP license metric for Oracle WebLogic Standard and WebLogic Enterprise on Oracle Authorized Cloud Environments such as AWS or Azure Cloud. For the Standard edition, a minimum of 10 NUP licenses are required per 8 vCPUs on either AWS or Azure Cloud. For the Enterprise edition, if hyper-threading is enabled then 10 NUP licenses are required per 2 vCPUs, and if hyper-threading is not enabled then 10 NUP licenses are required per vCPU.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Minimum NUPs per server

</td><td>

10

</td><td>

False

</td><td>

If licensed by NUP, Oracle Database Standard Edition 2 requires a minimum of 10 NUP licenses per server.

</td><td>

Named User Plus

</td><td>

Oracle

</td></tr><tr><td>

Maximum cores per processor

</td><td>

 

</td><td>

True

</td><td>

One license is required per CPU up to the physical core per CPU maximum. If a CPU has more physical cores than the maximum, additional CPU licenses are required.

 `Licenses required = Processors * (Cores/Maximum cores per processor)`

</td><td>

Per Processor

</td><td>

IBM

</td></tr><tr><td>

Maximum cores per processor

</td><td>

 

</td><td>

True

</td><td>

One license is required per CPU up to the physical core per CPU maximum. If a CPU has more physical cores than the maximum, additional CPU licenses are required.

 `Licenses required = Processors * (Cores/Maximum cores per processor)`

</td><td>

Per Processor

</td><td>

Citrix

</td></tr><tr><td>

Maximum cores per processor

</td><td>

32

</td><td>

False

</td><td>

Effective April 2, 2020, VMware requires one license for up to 32 physical cores. If a CPU has more than 32 cores, additional CPU licenses are required.

 `Licenses required = Processors * (Cores/Maximum cores per processor)`

</td><td>

Per Processor

</td><td>

VMware

</td></tr><tr><td>

Maximum cores per processor

</td><td>

 

</td><td>

True

</td><td>

One license is required per CPU up to the physical core per CPU maximum. If a CPU has more physical cores than the maximum, additional CPU licenses are required.

 `Licenses required = Processors * (Cores/Maximum cores per processor)`

</td><td>

Per Processor

</td><td>

Common

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Device

</td><td>

Adobe

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Device

</td><td>

IBM

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Device

</td><td>

Microsoft

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Device

</td><td>

Citrix

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Device

</td><td>

Common

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per Device

</td><td>

VMware

</td></tr><tr><td>

Minimum cores per VM

</td><td>

4

</td><td>

False

</td><td>

The number of core rights that must be applied to a virtual machine.

</td><td>

Per Core

</td><td>

Microsoft

</td></tr><tr><td>

Minimum cores per processor

</td><td>

4

</td><td>

False

</td><td>

The number of core rights that must be applied to a physical processor or set of vCores.

</td><td>

Per Core

</td><td>

Microsoft

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per User

</td><td>

Adobe

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per User

</td><td>

Microsoft

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per User

</td><td>

IBM

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per User

</td><td>

Citrix

</td></tr><tr><td>

Maximum installs per right

</td><td>

 

</td><td>

True

</td><td>

The maximum number of installs each right can license.

</td><td>

Per User

</td><td>

Common

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

