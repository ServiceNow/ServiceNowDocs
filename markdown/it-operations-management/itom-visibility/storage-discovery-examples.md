---
title: Storage discovery examples
description: Discovery creates configuration items \(CI\) and CI relationships for physical and logical storage components attached directly to application and database servers or by fibre channel switched fabric in a multi-path configuration.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Storage discovery examples

Discovery creates configuration items \(CI\) and CI relationships for physical and logical storage components attached directly to application and database servers or by fibre channel switched fabric in a multi-path configuration.

## Direct attached storage

In this example of direct attached storage \(DAS\), a SCSI drive with two partitions, `/dev/sda1` and `/dev/sda2`, is attached to a Linux host. The `/dev/sda1` partition is bootable and supports the system software. The `/dev/sda2` partition contains a logical volume configured as a storage pool and mounted to the Linux root file system by Logical Volume Management \(LVM\). The storage pool uses only 1.5GB of the partition, leaving 13GB of storage available for additional logical volumes.

<table id="table_t5y_fgq_mz"><thead><tr><th>

Configuration item

</th><th>

Description

</th><th>

Tables

</th><th>

Key reference and Relationships

</th></tr></thead><tbody><tr><td rowspan="2">

/dev/sda

</td><td rowspan="2">

SCSI physical storage device

</td><td rowspan="2">

-   \[cmdb\_ci\_disk\]
-   \[cmdb\_ci\_storage\_device\]
-   \[cmdb\_rel\_ci\]

</td><td>

\[cmdb\_rel\_ci\]-   **Provides**: /dev/sda
-   **Provided by:**/dev/sda1

</td></tr><tr><td>

\[cmdb\_rel\_ci\]-   **Provides**: /dev/sda
-   **Provided by:**/dev/mapper/lvm-root-333-0

</td></tr><tr><td rowspan="2">

/dev/sda1

</td><td rowspan="2">

Partition 1 on the SCSI storage device

</td><td rowspan="2">

-   \[cmdb\_ci\_partition\]
-   \[cmdb\_ci\_storage\_volume\]
-   \[cmdb\_ci\_file\_system\]
-   \[cmdb\_rel\_ci\]

</td><td>

\[cmdb\_ci\_file\_system\]-   **Mount point**: /boot
-   **File system**: Ext4

</td></tr><tr><td>

\[cmdb\_rel\_ci\]-   **Provides**: /dev/sda
-   **Provided by:**/dev/sda1

</td></tr><tr><td>

/dev/sda2

</td><td>

Partition 2 on the SCSI storage device

</td><td>

-   \[cmdb\_ci\_partition\]
-   \[cmdb\_ci\_storage\_pool\_member\]

</td><td>

\[cmdb\_ci\_storage\_pool\_member\]-   **Pool**: /dev/mapper/lvm-root-333-0
-   **Storage**: /dev/sda2

</td></tr><tr><td rowspan="3">

/dev/mapper/lvm-root-333-0

</td><td rowspan="3">

Linux logical volume, mapped with LVM to a physical disk storage partition.

</td><td rowspan="3">

-   \[cmdb\_ci\_storage\_device\]
-   \[cmdb\_ci\_storage\_volume\]
-   \[cmdb\_ci\_file\_system\]
-   \[cmdb\_ci\_storage\_pool\]
-   \[cmdb\_ci\_storage\_pool\_member\]
-   \[cmdb\_ci\_lvm\_pool\]
-   \[cmdb\_ci\_lvm\_pool\_member\]\[cmdb\_rel\_ci\]

</td><td>

\[cmdb\_ci\_file\_system\]-   **Mount point**: /
-   **File system**: Ext4

</td></tr><tr><td>

\[cmdb\_rel\_ci\]-   **Provides**: /dev/sda
-   **Provided by:**/dev/mapper/lvm-root-333-0

</td></tr><tr><td>

\[cmdb\_ci\_storage\_pool\_member\]-   **Pool**: /dev/mapper/lvm-root-333-0
-   **Storage**: /dev/sda2

</td></tr></tbody>
</table>## Multipath fibre channel storage

In this example of a fibre channel storage area network \(SAN\), two physical storage devices, `mpatha` and `mpathb`, are attached to a Linux host through fibre switches, which provide failover capabilities. The `mpatha` drive contains two partitions, `mpatha1` and `mpatha2`. The first partition is mounted directly to `/boot` on the Linux host. Three logical volumes are mapped to the `mpatha2` partition and to the physical device `mpathb`. The logical volumes are mounted as Ext4 file systems in folders on the Linux root structure. This example shows the CIs that Discovery manages for each component and the mounting points for the logical volumes on the Linux host.

## Switched fibre fabric details

Discovery creates CIs for the logical sub-components in NAS and SAN environments, such as fibre channel disks and pool components, as well as for host bus adapters \(HBA\) and physical block storage. In multipath environments, Discovery creates CI relationships within the switched fibre fabrics that connects the Linux host to the physical storage devices. In this diagram, the fibre fabrics have redundant paths that the SAN environment can use for failover if connections fail.

**Parent Topic:**[Storage discovery](../concept/c_Storage.md)

