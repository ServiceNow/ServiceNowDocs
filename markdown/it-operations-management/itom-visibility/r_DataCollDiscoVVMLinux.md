---
title: Data collected for Veritas Volume Manager on Linux
description: Discovery collects disk and volume information for Veritas Volume Manager \(VxVM\) on Linux hosts and maps file systems mounted on Veritas volumes to the upstream storage provider.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Data collected for Veritas Volume Manager on Linux

Discovery collects disk and volume information for Veritas Volume Manager \(VxVM\) on Linux hosts and maps file systems mounted on Veritas volumes to the upstream storage provider.

**Note:** Ensure that VxVM is correctly installed and configured. If you are using 3rd party drivers, you must configure sudo permission for `vxdmpadm`.

## Table schema

|Table|Extends table|
|-----|-------------|
|Veritas Disk \[cmdb\_ci\_veritas\_disk\]|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|Veritas Disk Group \[cmdb\_ci\_veritas\_disk\_group\]|Configuration Item \[cmdb\_ci\]|
|Veritas Plex \[cmdb\_ci\_veritas\_plex\]|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|Veritas Subdisk \[cmdb\_ci\_veritas\_subdisk\]|Storage Pool Member \[cmdb\_ci\_storage\_pool\_member\]|
|Veritas Volume \[cmdb\_ci\_veritas\_volume\]|Storage Pool \[cmdb\_ci\_storage\_pool\]|

## Data collected

<table id="table_ivg_bxz_bt"><thead><tr><th>

Table

</th><th>

Fields

</th><th>

Relationship

</th></tr></thead><tbody><tr><td>

Veritas Disk \[cmdb\_ci\_veritas\_disk\]

</td><td>

-   name
-   size\_bytes
-   disk\_group

</td><td>

Provided by::Provides relationship to the physical disk.

</td></tr><tr><td>

Veritas Disk Group \[cmdb\_ci\_veritas\_disk\_group\]

</td><td>

name

</td><td>

Contains::Contained by relationship to Veritas Disks in the group.

</td></tr><tr><td>

Veritas Plex \[cmdb\_ci\_veritas\_plex\]

</td><td>

-   name
-   size\_bytes
-   layout \(CONCAT, STRIPE, RAID\)

</td><td>

 

</td></tr><tr><td>

Veritas Subdisk \[cmdb\_ci\_veritas\_subdisk\]

</td><td>

-   partition\_number
-   source\_start\_offset: Offset in the disk from which this subdisk is partitioned.
-   source\_end\_offset: Offset in the disk from which this subdisk is partitioned.
-   start\_offset: Offset of this subdisk in the plex that is using it.
-   end\_offset: Offset of this subdisk in the plex that is using it.
-   size\_bytes

</td><td>

 

</td></tr><tr><td>

Veritas Volume \[cmdb\_ci\_veritas\_volume\]

</td><td>

name

</td><td>

Stored on::Provides storage for relationship to Veritas Disks on which the volume is stored.

</td></tr></tbody>
</table>## Displaying data

VxVM Discovery maps file systems to the disks that supply storage. By default this is the only information displayed in the UI. The file system to disk relationship is shown as an upstream **Stored on** relationship on the File System form. To see the remainder of the information that Discovery captures for VxVM, you must add the appropriate related list to the Linux Server form. The available lists are:

-   Veritas Disk Group
-   Veritas Disk
-   Veritas Plex
-   Veritas Subdisk \(Computer\)
-   Veritas Subdisk \(Storage\)
-   Veritas Volume

**Parent Topic:**[Storage discovery](../concept/c_Storage.md)

