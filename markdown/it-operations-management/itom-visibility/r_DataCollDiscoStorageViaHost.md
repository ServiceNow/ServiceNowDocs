---
title: Discovery data collected for storage via a host
description: Discovery gathers information about storage units that connect to Linux, Solaris, and Windows hosts via a local I/O port or Host Bus Adapter \(HBA\).
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Discovery data collected for storage via a host

Discovery gathers information about storage units that connect to Linux, Solaris, and Windows hosts via a local I/O port or Host Bus Adapter \(HBA\).

## Probes used to discover storage from a host

<table id="table_r51_k4m_ns"><thead><tr><th>

Table

</th><th>

Probes

</th></tr></thead><tbody><tr><td>

Disk \[cmdb\_ci\_disk\]

</td><td>

-   KVM
-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Disk Partition \[cmdb\_ci\_disk\_partition\]

</td><td>

-   KVM
-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Fibre Channel Disk \[cmdb\_ci\_fc\_disk\]

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008

</td></tr><tr><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008

</td></tr><tr><td>

File System \[cmdb\_ci\_file\_system\]

</td><td>

-   KVM
-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

iSCSI Disk \[cmdb\_ci\_iscsi\_disk\]

</td><td>

-   KVM
-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

NAS File System \[cmdb\_ci\_nas\_file\_system\]

</td><td>

-   KVM
-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008

</td></tr><tr><td>

Storage Pool \[cmdb\_ci\_storage\_pool\]

</td><td>

Linux - Storage

</td></tr><tr><td>

Storage Pool Member \[cmdb\_ci\_storage\_pool\_member\]

</td><td>

Linux - Storage

</td></tr><tr><td>

VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]

</td><td>

VMware - vCenter Datastores

</td></tr></tbody>
</table>## Storage references discovered

Discovery maps these references for storage units that connect to a host via a local I/O port or Host Bus Adapter \(HBA\).

|Table and column|Reference|Target data element|
|----------------|---------|-------------------|
|cmdb\_ci\_storage\_device.computer|refers to the|cmdb\_ci\_computer|
|cmdb\_ci\_storage\_device.provided\_by|refers to the|cmdb\_ci\_fc\_port \(for FC only\)|
|cmdb\_ci\_disk\_partition.disk|is a partition of|cmdb\_ci\_disk|
|cmdb\_ci\_storage\_hba.computer|is the|cmdb\_ci\_computer|
|cmdb\_ci\_fc\_port.controller|contains the|cmdb\_ci\_storage\_hba|
|cmdb\_ci\_fc\_port.computer|is the same|cmdb\_ci\_computer as cmdb\_ci\_storage\_hba.computer|
|cmdb\_ci\_storage\_volume.computer|is the|cmdb\_ci\_computer|
|cmdb\_ci\_storage\_volume.provided\_by|is the|cmdb\_ci\_storage\_pool or cmdb\_ci\_storage\_pool or cmdb\_ci\_storage\_device \(providing storage\)|
|cmdb\_ci\_storage\_pool.hosted\_by|is the|cmdb\_ci\_computer|
|cmdb\_ci\_computer|the pool is on|cmdb\_ci\_storage\_pool.container|
|cmdb\_ci\_storage\_pool.container|is the|cmdb\_ci\_storage\_pool or cmdb\_ci\_storage\_pool\_member containing the pool \(if the pool is present\)|
|cmdb\_ci\_storage\_pool\_member.pool|is the|cmdb\_ci\_storage\_pool|
|cmdb\_ci\_storge\_pool\_member.storage|is the|cmdb\_ci\_storage\_pool, cmdb\_ci\_disk\_partition or cmdb\_ci\_storage\_device providing storage|

## Data collected for HBAs on Linux and ESX servers

Discovery collects information on host bus adapters \(HBA\) for fiber channel enabled devices connected to Linux and ESX servers.

<table id="table_bvr_2ys_lp"><thead><tr><th>

Label

</th><th>

Table

</th><th>

Field name

</th><th>

Source

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

name

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr><tr><td>

WWNN

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

wwnn

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr><tr><td>

Model ID

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

model\_id

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr><tr><td>

Computer

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

computer

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr></tbody>
</table><table id="table_tzj_3xd_gs"><thead><tr><th>

Label

</th><th>

Table

</th><th>

Field name

</th><th>

Source

</th></tr></thead><tbody><tr><td>

WWPN

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

wwpn

</td><td>

VMWare - vCenter ESX Hosts Storage-   probe
-   Linux - Storage

</td></tr><tr><td>

WWNN

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

wwnn

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr><tr><td>

Port type

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

port\_type

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr><tr><td>

Speed

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

speed

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr><tr><td>

Controller

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

controller

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr><tr><td>

Computer

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

computer

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Linux - Storage

</td></tr></tbody>
</table><table id="table_fxj_p5s_nt"><thead><tr><th>

Label

</th><th>

Table

</th><th>

Field name

</th><th>

Source

</th></tr></thead><tbody><tr><td>

FC Disk

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

fc\_disk

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Created by

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

sys\_created\_by

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Created

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

sys\_created\_on

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

SysID

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

sys\_id

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Updates

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

sys\_mod\_count

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Updated by

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

sys\_updated\_by

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Updated

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

sys\_updated\_on

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

WWNN

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

wwnn

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

WWPN

</td><td>

Fibre Channel Targets \[cmdb\_fc\_target\]

</td><td>

wwpn

</td><td>

-   Linux - Storage
-   Solaris - Storage
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr></tbody>
</table>## Data collected for HBAs on Solaris servers

Discovery on Solaris supports HBAs manufactured by:

-   Emulex
-   QLogic

Discovery populates these fields in the Storage HBA \[cmdb\_ci\_storage\_hba\] table, using the Solaris - Storage probe and sensor.

|Label|Field name|
|-----|----------|
|Name|name|
|Computer|computer|
|Device ID|device\_id|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Serial number|serial\_number|

Discovery populates these fields in the Fibre Channel Port \[cmdb\_ci\_fc\_port\] table.

|Label|Field name|
|-----|----------|
|Name|name|
|Computer|computer|
|Controller|controller|
|WWPN|wwpn|
|WWNN|wwnn|
|Port type|port\_type|
|Speed|speed|
|Operational status|operational\_status|

Discovery populates these fields in the Fibre Channel Disk \[cmdb\_ci\_fc\_disk\] table.

|Label|Name|
|-----|----|
|Name|name|
|Storage type|storage\_type|
|Device interface|device\_interface|
|Device LUN|device\_lun|

Discovery populates these fields in the Fibre Channel Targets \[cmdb\_fc\_target\] table.

|Label|Name|
|-----|----|
|FC Disk|fc\_disk|
|WWNN|wwnn|
|WWPN|wwpn|

## Data collected for HBAs on Windows servers

Discovery on Windows supports HBAs on any operating system.

<table id="table_avr_2ys_lp"><thead><tr><th>

Label

</th><th>

Table

</th><th>

Field Name

</th><th>

Source

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

name

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

WWNN

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

wwnn

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Model ID

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

model\_id

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Computer

</td><td>

Storage HBA \[cmdb\_ci\_storage\_hba\]

</td><td>

computer

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr></tbody>
</table><table id="table_tzo_3xd_gs"><thead><tr><th>

Label

</th><th>

Table

</th><th>

Field Name

</th><th>

Source

</th></tr></thead><tbody><tr><td>

WWPN

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

wwpn

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

WWNN

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

wwnn

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Port type

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

port\_type

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Speed

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

speed

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Controller

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

controller

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr><tr><td>

Computer

</td><td>

Fibre Channel Port \[cmdb\_ci\_fc\_port\]

</td><td>

computer

</td><td>

-   VMWare - vCenter ESX Hosts Storage probe
-   Windows - Storage 2008
-   Windows - Storage 2012

</td></tr></tbody>
</table>**Parent Topic:**[Storage discovery](../concept/c_Storage.md)

