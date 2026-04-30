---
title: Sizing your Edge Encryption environment
description: Choosing the number of proxy servers for your environment is an important task. Consider the number of users, redundancy needs, and acceptable latency.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Planning for Edge Encryption, Edge Encryption, Encryption]
---

# Sizing your Edge Encryption environment

Choosing the number of proxy servers for your environment is an important task. Consider the number of users, redundancy needs, and acceptable latency.

## Redundancy

Maintain redundant proxy servers in case of hardware failure. Proxy servers should be located behind a load balancer to provide a functional path for all users if a proxy server is unreachable. At a minimum, ensure that two proxy servers are always available.

## Size

Size refers to the number of proxy servers required to avoid additional latency that the encryption of data produces. Depending on use, you may want to reduce the amount of latency by adding additional proxy servers. For example, if regular mass encryptions are run, add additional proxy servers to handle the load, or run the mass encryptions when the user load is light. In addition, the hardware that the proxy server runs on influences performance and latency. Proxy servers running on hardware with faster CPUs, more CPUs, and more RAM have higher throughput than slower, limited systems.

The following guidelines assume that your proxy server is running on at least the minimum hardware requirements. To determine the number of proxy servers:

-   Consider setting up one proxy server for every two application nodes on the instance.
-   For redundancy, set up a minimum of two proxy servers behind a load balancer.
-   Add an extra proxy server for every 500 simultaneous users.
-   Depending on the desired redundancy, add additional proxy servers for failover.

For example, for an instance with 2,000 users, you should have at least five proxy servers behind a load balancer. This calculation includes one proxy server for every 500 users, with an extra proxy server for failover. Determine ahead of time when you will approach a threshold of 500 users and place another proxy server in the load balancer pool.

## Load balancers

To balance requests and improve server response time, distribute proxy servers in a load balancer pool. Configure load balancers to use the "least connections" method. This method connects requests to the proxy server with the fewest active connections, preventing the overloading of a single proxy.

## CPU utilization

Because data encryption and tokenization are CPU intensive operations, CPU spikes while encrypting data are normal and expected. When CPU utilization is over 80% for several minutes at a time, it likely means that the proxy server has too much work to do. When this happens, latency increases for the period that the CPU utilization is high. If latency persists, adding another proxy server may help decrease the latency.

## Memory

The proxy server must have a minimum of 4 GB of RAM available \(6 GB recommended\). [Set the proxy server initial and upper bound memory limits](../task/increase-memory.md) to the recommended settings.

**Parent Topic:**[Planning for Edge Encryption](c_EdgeEncryptionPlanning.md)

