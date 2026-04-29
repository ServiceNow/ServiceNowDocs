---
title: Windows server cluster discovery
description: Discovery establishes the relationships between a Windows server cluster and its nodes.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Windows, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Windows server cluster discovery

Discovery establishes the relationships between a Windows server cluster and its nodes.

When a Windows server is found, and Discovery detects that it is part of a cluster, the system launches the Windows - Cluster probe. Navigate to **Discovery Definition** &gt; **Probes** and open the record for the Windows - Cluster probe to see the specific data Discovery collects.

**Note:** Discovery collects cluster resources based on the MSCluster\_ResourceType WMI class. To see a list of default cluster resources, see [Resource Types](https://msdn.microsoft.com/en-us/library/windows/desktop/aa372279(v=vs.85).aspx). To understand how cluster resources are related to process classifiers, see [Relate the process classifier to Windows cluster resources](../concept/c_ClusteredAppDiscoveryOnWindows.md#).

## Cluster data tables

Discovery creates CIs for clusters in these tables:

-   Windows Cluster \[cmdb\_ci\_win\_cluster\]
-   Windows Cluster Resource\(s\) \[cmdb\_ci\_win\_cluster\_resource\]
-   Windows Cluster Node\(s\) \[cmdb\_ci\_win\_cluster\_node\]
-   Cluster Node Resource\(s\) \[cmdb\_ci\_cluster\_node\_resource\]
-   Cluster Virtual IP\(s\) \[cmdb\_ci\_cluster\_vip\]

## Cluster relationships

Discovery creates a CI Relationship \[cmdb\_rel\_ci\] record for each node, using these relationships:

-   **Cluster of::Cluster**: Relationship between the cluster nodes and the cluster. [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md) uses this relationship to map the Windows cluster and it's nodes.
-   **Members::Member of**: Relationship between the cluster and the cluster node.
-   **Hosted on::Hosts**: Relationship between the cluster nodes and the Windows server.
-   **Uses::Used by**: Cluster VirtualIP and Windows Cluster Node.
-   **Defines resources for::Gets resources from**: Windows Cluster Resources and Windows Cluster.
-   **Defines resources for::Gets resources from**: Windows Cluster Resources and Windows Cluster Node.

![Windows cluster map](../image/WindowsClusterMap.png "Windows cluster map")

![Windows cluster node relationships](../image/WinClusterNodeRelationships.png "Windows cluster node relationships")

## Cluster references

Discovery creates the following cluster references:

-   From Windows Cluster Nodes to the associated Windows Cluster.
-   From Windows Cluster Resources to the associated Windows Cluster.
-   From Cluster Virtual IPs to the associated Windows Cluster.
-   From Cluster Node Resources to the associated Windows Cluster Node.
-   From Cluster Virtual IPs to the associated Windows Cluster Node.

**Note:** References are maintained in Discovery to provide backward compatibility for systems that use them.

**Parent Topic:**[Windows discovery](r_DataCollDiscoWindowsComputers.md)

