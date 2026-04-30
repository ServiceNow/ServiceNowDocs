---
title: Red Hat Enterprise Linux socket-pair based licensing
description: Use the RHEL Server licensing based on the number of socket-pairs or virtual machine \(VM\) pairs on a physical host to manage licenses for your RHEL products.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Software Asset Management for Red Hat Enterprise Linux, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Red Hat Enterprise Linux socket-pair based licensing

Use the RHEL Server licensing based on the number of socket-pairs or virtual machine \(VM\) pairs on a physical host to manage licenses for your RHEL products.

## Overview of the socket-pair based licensing model

-   **Red Hat Enterprise Linux Server**

    Red Hat Enterprise Linux Server enables Linux distributions in physical, virtual, and hybrid environments. Although you can use RHEL licenses in both low-density and high-density virtual environments, they’re more cost efficient in low-density virtual environments.

    To determine whether a virtual environment is low-density or high-density, divide the number of required RHEL licenses by the number of required RHEL for Virtual Datacenters licenses. Compare this value against the threshold value in the **Red Hat Enterprise Linux for Virtual Datacenters license cost optimization threshold** field that you defined in your [Software Asset Management properties](../reference/sam-properties.md). If your value is lower than the threshold value, then the virtual environment is considered low-density. If your value is equal to or higher than the threshold value, then the virtual environment is considered high density.

    **Note:** The default value for the **Red Hat Enterprise Linux for Virtual Datacenters license cost optimization threshold** field is 3.2. This value is based on the ratio of the current RHEL Server subscription list price to the current RHEL for Virtual Datacenters subscription list price. If your entitlements contain different pricings for these products, then you can calculate this value by dividing your RHEL for Virtual Datacenters subscription price by your RHEL Server subscription price.

    RHEL uses different licensing models depending on the environment in which you deploy a server.

<table id="table_bzb_3dg_4nb"><thead><tr><th>

Environment

</th><th>

Description

</th><th>

Licensing model

</th><th>

Cluster licensing model

</th></tr></thead><tbody><tr><td>

Physical

</td><td>

Deployment of RHEL servers on physical hosts.

</td><td>

Licensing is based on the number of socket-pairs on the physical host. For example, a physical host with 10 sockets requires five RHEL Server licenses.Single-socket hosts must be licensed individually.

</td><td>

Licensing is based on the total number of socket-pairs on the physical hosts within a cluster. For example, if Cluster Host A has 10 sockets and Cluster Host B has 20 sockets, then you must use 15 RHEL Server licenses to license the entire cluster.

</td></tr><tr><td>

Virtual \(low-density and high density\)

</td><td>

Deployment of RHEL servers on the VMs that are running on physical hosts.

</td><td>

Licensing is based on the number of VM pairs that are running the server on a physical host. For example, a physical host with six VMs that are running a RHEL server requires three RHEL Server licenses.Single VMs that are running a RHEL server must be licensed individually.

</td><td>

Licensing is based on the total number of VM pairs on the physical hosts within a cluster. For example, if Cluster Host A has 10 VMs and Cluster Host B has 20 VMs, you must use 15 RHEL Server licenses to license the entire cluster.

</td></tr><tr><td>

Hybrid

</td><td>

Deployment of RHEL servers on the physical hosts and on the VMs that are running on those hosts.

</td><td>

Licensing is based on the number of socket-pairs on the physical host and the number of VM pairs that are running the server on the same host. For example, you can run a RHEL server on a physical host with 10 sockets and also on the 20 VMs running on that host. In this example, the host requires a total of 15 RHEL Server licenses.

</td><td>

Licensing is based on the total number of socket-pairs and VM pairs on the physical hosts within a cluster. For example, if Cluster Host A has 10 sockets and 10 VMs while Cluster Host B has 20 sockets and 20 VMs, you must use 30 RHEL Server licenses to license the entire cluster.

</td></tr></tbody>
</table>-   **Red Hat Enterprise Linux for Virtual Datacenters**

    Red Hat Enterprise Linux for Virtual Datacenters uses hypervisors, such as Red Hat Virtualization and VMware, to enable Linux distributions in both low-density and high-density virtual environments. RHEL for Virtual Datacenters licenses are more cost efficient in high-density virtual environments.

    To determine whether a virtual environment is low-density or high-density, divide the number of required RHEL Server licenses by the number of required RHEL for Virtual Datacenters licenses. Compare this value against the threshold value in the **Red Hat Enterprise Linux for Virtual Datacenters license cost optimization threshold** field that you defined in your [Software Asset Management properties](../reference/sam-properties.md). If your value is lower than the threshold value, then the virtual environment is considered low-density. If your value is equal to or higher than the threshold value, then the virtual environment is considered high density.

    **Note:** The default value for the **Red Hat Enterprise Linux for Virtual Datacenters license cost optimization threshold** field is 3.2. This value is based on the ratio of the current RHEL Server subscription list price to the current RHEL for Virtual Datacenters subscription list price. If your entitlements contain different pricings for these products, you can calculate this value by dividing your RHEL for Virtual Datacenters subscription price by your RHEL Server subscription price.

    RHEL for Virtual Datacenters licensing is based on the number of socket-pairs on the physical hosts that are running your VMs. With this license type, you don’t need to license the VMs that are running a RHEL for Virtual Datacenters server because you can access an unlimited number of VMs from your physical hosts. Single-socket hosts must be licensed individually.

    If you deploy a RHEL for Virtual Datacenters server on VMs within a cluster, licensing is based on the total number of socket-pairs on all hosts that are running those VMs. Since you can access an unlimited number of VMs from your physical hosts, you don’t need to license the cluster based on the total number of VMs that are running the server within the cluster. For example, if Cluster Host A has 10 sockets and 20 VMs while Cluster Host B has 20 sockets and 60 VMs, you must use 15 RHEL for Virtual Datacenters licenses to license the entire cluster.


## License consumption order

If you have both RHEL Server and RHEL for Virtual Datacenters licenses, consume them in the following order:

1.  RHEL for Virtual Datacenters licenses on the physical hosts, VMs, or clusters that have allocated licenses.
2.  RHEL Server licenses on the physical hosts, VMs, or clusters that have allocated licenses.
3.  RHEL for Virtual Datacenters licenses on physical hosts, VMs, or clusters in high-density virtual environments.
4.  RHEL Server licenses on physical hosts, VMs, or clusters in low-density virtual environments.
5.  RHEL Server licenses on physical hosts, VMs, or clusters in high-density virtual environments. Use this license type only if you have run out of RHEL for Virtual Datacenters licenses in high-density virtual environments.
6.  RHEL for Virtual Datacenters licenses on physical hosts, VMs, or clusters in low-density virtual environments. Use this license type only if you have run out of RHEL Server licenses in low-density virtual environments.

**Parent Topic:**[Software Asset Management for Red Hat Enterprise Linux](rhel-publisher-pack.md)

