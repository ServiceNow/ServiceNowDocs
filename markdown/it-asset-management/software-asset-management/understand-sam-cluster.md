---
title: Understanding your cluster infrastructure
description: Get a holistic and strategic analysis of all the entities in your clusters in one view on the Software Asset Management application.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Understanding your cluster infrastructure

Get a holistic and strategic analysis of all the entities in your clusters in one view on the Software Asset Management application.

The SAM Cluster 360° feature simplifies the process of analyzing a cluster, which is typically a time-consuming task. This feature helps SAM managers to make strategic decisions by providing them with a visually comprehensive view of their cluster setup, licensing, and cluster health issues. Drill down to each node on a cluster for a deeper understanding. For detailed information on your cluster, see [View your cluster setup in 360 degrees](../task/view-360-sam-cluster.md).

## Cluster overview

A cluster is a type of virtualization where hosts are grouped and share resources. This technology provides high availability, resource pooling, and load balancing for virtual machines that run on it. This technology provides the foundation for building highly resilient, scalable, and efficient virtualized environments.

Each host has the capacity to run multiple virtual machines \(VMs\) and can be configured to support features such as high availability, DRS \(Dynamic Resource Scheduling\), and host affinity.

The VMs can move across the hosts depending on certain settings such as High availability or Distributed Resource Scheduler \(DRS\). Settings such as Host affinity can lock VMs to certain hosts.

Factors such as the number of VMs, movement of VMs, hosts, and VM cores in a cluster can affect your license compliance.

![Cluster setup](../image/cluster-details.png "Cluster setup")

## Benefits of SAM Cluster 360°

SAM Cluster 360° provides a holistic and strategic analysis of clusters to support infrastructure understanding, license compliance, and health checks across the cluster.

The SAM Cluster 360° feature helps you to view and analyze the following concepts:

-   Core infrastructure of a cluster: hosts, VMs, software, cores, and processors.
-   All hosts and the VMs that can potentially move on them.
-   All software, licensable and non-licensable, running on a cluster.
-   All software consuming licenses.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

