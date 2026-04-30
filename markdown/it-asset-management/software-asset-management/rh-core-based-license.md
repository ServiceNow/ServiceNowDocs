---
title: Red Hat Enterprise Linux core-based licensing
description: Use the RHEL Per Core license metric to license core-based RHEL products on both physical and virtual environments.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Software Asset Management for Red Hat Enterprise Linux, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Red Hat Enterprise Linux core-based licensing

Use the RHEL Per Core license metric to license core-based RHEL products on both physical and virtual environments.

## Overview of the Per Core licensing model

To license a software product under the Per Core licensing model, each server must be assigned an appropriate number of core licenses. The number of core licenses needed depends on whether you’re licensing the physical server or an individual virtual operating system environment \(OSE\).

Licensing under the Per Core model offers the following benefits:

-   Tracks core packs for Red Hat products.
-   Imports entitlements with the number of rights per license pack and the number of packs for Red Hat core-based entitlements.
-   Enables customers to enter the number of rights per license pack and the number of packs for any Red Hat core-based product​.
-   Calculates the purchased rights based on the number of rights per license pack multiplied by the number of packs.
-   Creates and removes allocations based on reconciliation of Red Hat core-based products​.

Allocations can be applied to virtual machines \(VM\) or only to hosts. This metric runs calculations for physical cores and virtual cores on each machine and presents the most optimal licensing model based on the number of rights used.

## Total license requirement calculation

Total license requirement is calculated at the physical host level. The following table includes examples of the various use cases for total license requirement:

<table id="table_r5d_v2d_nzb"><thead><tr><th>

Environment

</th><th>

Description

</th><th>

License requirement

</th></tr></thead><tbody><tr><td>

Physical

</td><td>

Deployment of RHEL core-based products on physical machines.

</td><td>

Licensing is based on the total number of physical cores on the machine. The total number can be found by multiplying the number of sockets by the number of cores per socket.For example, say that a physical machine has 2 sockets and 8 cores per socket. Multiplying 2 by 8 would mean that the total number of physical cores would be 16. `2*8 = 16` Thus, the total number of rights required is 16 cores.

</td></tr><tr><td>

Virtual

</td><td>

Deployment of RHEL core-based products on the VMs that run on physical hosts.

</td><td>

Licensing is based on the total number of cores assigned to the VMs that run the server on a physical host. This number is limited to the maximum capacity of the physical host.For example, say that a physical host has 2 sockets with 8 cores per socket and 6 VMs with 2 cores per VM. Each VM has installed a RHEL core-based product. In this case, the number of rights required equals the minimum value between the physical core capacity of the physical host and the number of non-hyperthreaded physical cores assigned to VMs. 2 sockets multiplied by 8 cores per socket equal 16 cores, and 6 VMs multiplied by 2 cores per VM equal 12 cores. The minimum value between the two is 12 cores. `Min(2*8 = 16, 2*6 = 12)` Thus, the total number of rights required is 12 cores.

</td></tr><tr><td>

Hybrid

</td><td>

Deployment of RHEL core-based products on the physical hosts and on the VMs that run on those physical hosts.

</td><td>

Licensing is based on the number of physical cores on which the RHEL core-based application is installed. For example, a physical host has 2 sockets with 8 cores per socket and 20 VMs with 2 cores per VM. A RHEL core-based product is installed on the physical host and all 20 VMs. In this case, the number of rights required is the minimum value between the physical core capacity of the physical host and the number of non-hyperthreaded physical cores assigned to VMs added to the number of physical hosts. 2 sockets multiplied by 8 cores per socket equal 16 cores. Then, 2 cores multiplied by 8 cores equal 16 cores, and 20 VMs multiplied by 2 cores per VM equal 40 cores. Add 16 cores to 40 cores, and it equals 56 cores. The minimum value between the two is 16 cores. `Min((2*8) = 16, (2*8 + 2*20) = 56)` Thus, the total number of rights required is 16 cores.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management for Red Hat Enterprise Linux](rhel-publisher-pack.md)

