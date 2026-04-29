---
title: Red Hat Enterprise Linux socket-pair based licensing
description: The Software Asset Management publisher pack for IBM supports socket-pair based licensing rules for Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Software Asset Management for Red Hat Enterprise Linux, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Red Hat Enterprise Linux socket-pair based licensing

The Software Asset Management publisher pack for IBM supports socket-pair based licensing rules for Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters.

## Overview of the socket-pair based licensing model

-   **Red Hat Enterprise Linux Server**

    Red Hat Enterprise Linux Server enables Linux distributions in physical, virtual, and hybrid environments. Although you can use RHEL licenses in both low-density and high-density virtual environments, they’re more cost efficient in low-density virtual environments.

    To determine whether a virtual environment is low-density or high-density, divide the number of required RHEL Server rights by the number of required RHEL for Virtual Datacenters rights. Compare this value against the threshold value in the **Red Hat Enterprise Linux for Virtual Datacenters license cost optimization threshold** field that you defined in your [Software Asset Management properties](../reference/sam-properties.md). If your value is lower than the threshold value, then the virtual environment is considered low-density. If your value is equal to or higher than the threshold value, then the virtual environment is considered high density.

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

</th><th>

Cloud licensing model

</th></tr></thead><tbody><tr><td>

Physical

</td><td>

Deployment of RHEL servers on physical hosts.

</td><td>

Licensing is based on the number of socket-pairs on the physical host that is running a RHEL server. Each socket-pair requires one right. For example, if you're running a RHEL server on a physical host with 10 sockets, you must use five rights to license the host.Single-socket hosts must be licensed individually. Each of these hosts requires one right.

</td><td>

Licensing is based on the total number of socket-pairs on all physical hosts that are running a RHEL server within a cluster. Each socket-pair requires one right. For example, if you're running a RHEL server on Cluster Host A, which has 10 sockets, and on Cluster Host B, which has 20 sockets, then you must use 15 rights to license the entire cluster.

</td><td>

N/A

</td></tr><tr><td>

Virtual \(low-density and high density\)

</td><td>

Deployment of RHEL servers on the VMs that are running on physical hosts.

</td><td>

Licensing is based on the number of VM pairs that are running a RHEL server within a physical host. Each VM pair requires one right. For example, if you're running a RHEL server on six VMs within a physical host, you must use three rights to license those VMs.Single VMs must be licensed individually. Each of these VMs requires 0.5 rights.

</td><td>

Licensing is based on the total number of VM pairs that are running a RHEL server within a cluster. For example, if you're running a RHEL server on a total of 10 VMs within a cluster, you must use five rights to license the entire cluster.

</td><td>

Licensing is based on the number of VMs that are running a RHEL server within a cloud environment. Each VM requires 0.5 rights. For example, if you're running a RHEL server on four VMs within a cloud environment, such as Amazon Web Services \(AWS\), you must use two rights to license those VMs.

</td></tr><tr><td>

Hybrid

</td><td>

Deployment of RHEL servers on physical hosts and on the VMs that are running on those hosts.

</td><td>

Licensing is based on a combination of the following:-   The number of socket-pairs on the physical host that is running a RHEL server.
-   The number of VM pairs that are running a RHEL server within that same physical host.
Each socket-pair and VM pair requires one right. For example, if you're running a RHEL server on a physical host with 10 sockets and on 20 VMs within that host, you must use a total of 15 rights to license the host and VMs.

</td><td>

Licensing is based on a combination of the following:-   The total number of socket-pairs on all physical hosts that are running a RHEL server within a cluster.
-   The total number of VM pairs that are running a RHEL server within that same cluster.
Each socket-pair and VM pair requires one right. For example, if you're running a RHEL server on Cluster Host A, which has 10 sockets; on Cluster Host B, which has 20 sockets; and on 10 VMs within Cluster Host A, you must use 20 rights to license the entire cluster.

</td><td>

Licensing is based on the number of VMs that are running a RHEL server within a cloud environment. Each VM requires 0.5 rights.**Note:** This licensing model is applicable only for RHEL servers that are running on VMs.

For example, if you're running a RHEL server on four VMs within a cloud environment, such as Amazon Web Services \(AWS\), you must use two rights to license those VMs.

</td></tr></tbody>
</table>-   **Red Hat Enterprise Linux for Virtual Datacenters**

    Red Hat Enterprise Linux for Virtual Datacenters uses hypervisors, such as Red Hat Virtualization and VMware, to enable Linux distributions in both low-density and high-density virtual environments. RHEL for Virtual Datacenters licenses are more cost efficient in high-density virtual environments.

    To determine whether a virtual environment is low-density or high-density, divide the number of required RHEL Server rights by the number of required RHEL for Virtual Datacenters rights. Compare this value against the threshold value in the **Red Hat Enterprise Linux for Virtual Datacenters license cost optimization threshold** field that you defined in your [Software Asset Management properties](../reference/sam-properties.md). If your value is lower than the threshold value, then the virtual environment is considered low-density. If your value is equal to or higher than the threshold value, then the virtual environment is considered high density.

    **Note:** The default value for the **Red Hat Enterprise Linux for Virtual Datacenters license cost optimization threshold** field is 3.2. This value is based on the ratio of the current RHEL Server subscription list price to the current RHEL for Virtual Datacenters subscription list price. If your entitlements contain different pricings for these products, you can calculate this value by dividing your RHEL for Virtual Datacenters subscription price by your RHEL Server subscription price.

    RHEL for Virtual Datacenters licensing is based on the total number of socket-pairs across all physical hosts within a cluster, regardless of whether or not the hosts are currently running VMs with installations. With this license type, you don’t need to license the VMs that are running a RHEL for Virtual Datacenters server because you can access an unlimited number of VMs from your physical hosts. Single-socket hosts must be licensed individually.

    **Note:** Although Red Hat permits you to license a subset of hosts when VM mobility is restricted, this licensing scenario is not currently supported by the Software Asset Management application.

    If you deploy a RHEL for Virtual Datacenters server on VMs within a cluster, licensing is based on the total number of socket-pairs on all hosts that are running those VMs. Since you can access an unlimited number of VMs from your physical hosts, you don’t need to license the cluster based on the total number of VMs that are running the server within the cluster. For example, if Cluster Host A has 10 sockets and 20 VMs while Cluster Host B has 20 sockets and 60 VMs, you must use 15 RHEL for Virtual Datacenters rights to license the entire cluster.


## License consumption order

If you have both RHEL Server and RHEL for Virtual Datacenters licenses, consume them in the following order:

1.  RHEL for Virtual Datacenters licenses on the physical hosts, VMs, or clusters that have allocated licenses.
2.  RHEL Server licenses on the physical hosts, VMs, or clusters that have allocated licenses.
3.  RHEL for Virtual Datacenters licenses on physical hosts, VMs, or clusters in high-density virtual environments.
4.  RHEL Server licenses on physical hosts, VMs, or clusters in low-density virtual environments.
5.  RHEL Server licenses on physical hosts, VMs, or clusters in high-density virtual environments. Use this license type only if you have run out of RHEL for Virtual Datacenters licenses in high-density virtual environments.
6.  RHEL for Virtual Datacenters licenses on physical hosts, VMs, or clusters in low-density virtual environments. Use this license type only if you have run out of RHEL Server licenses in low-density virtual environments.

**Parent Topic:**[Software Asset Management for Red Hat Enterprise Linux](rhel-publisher-pack.md)

