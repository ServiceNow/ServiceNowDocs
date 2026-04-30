---
title: Enabling access to a data source
description: Work with your data source administrator to enable access to your external data source.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Enabling access to a data source

Work with your data source administrator to enable access to your external data source.

To connect to a data source behind a private network using a zero copy connection, there are two general approaches:

-   **IP allowlist**

    Your data source admin must allow access to a source IP range based on where the zero copy queries are coming from. For help with identifying the correct IP range, contact your account manager or Customer Service and Support and reference KB1706533.

-   **Private connectivity**

    For data sources hosted behind private Virtual Private Clouds \(VPCs\) or Virtual Networks \(VNets\) in the public cloud, connectivity options are available that enable query traffic to transit over private IP address space, end to end. This private connectivity is enabled by technologies such as [Private Link](https://learn.microsoft.com/en-us/azure/private-link/private-link-overview). It’s important to note that each cloud provider implements this technology differently. To explore private connectivity options for your specific topology, contact your account manager or Customer Service and Support.


**Parent Topic:**[Configuring Workflow Data Fabric Hub](configuring-wdf.md)

