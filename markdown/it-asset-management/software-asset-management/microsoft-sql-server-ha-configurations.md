---
title: Microsoft SQL Server licensing in high availability configurations
description: The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft SQL Server deployed through high availability and disaster recovery solutions, such as Always On availability groups.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Microsoft SQL Server licensing in high availability configurations

The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft SQL Server deployed through high availability and disaster recovery solutions, such as Always On availability groups.

Always On availability groups provide high availability \(HA\) and disaster recovery capabilities for your Microsoft deployments. Each availability group consists of a primary replica, which hosts the database or server that you are actively running, and up to eight secondary replicas, which host the passive databases or servers that you can fail over to in the event that the primary replica fails. These availability groups support failover environments that can help you reduce and prevent downtime in your deployments. For more information on Always On availability groups, see [What is an Always On availability group?](https://learn.microsoft.com/en-us/sql/database-engine/availability-groups/windows/overview-of-always-on-availability-groups-sql-server?view=sql-server-ver17).

For each server operating system environment \(OSE\) that you’re licensing using either a Microsoft SQL Server subscription license or Microsoft SQL Server license with active Software Assurance \(SA\) benefits, you can use the following secondary \(passive\) replicas in anticipation of a failover event:

-   One secondary replica for high availability in a separate OSE
-   One secondary replica for disaster recovery in a separate OSE

The primary \(active\) replica is automatically licensed by the Microsoft SQL Server license. However, the two secondary replicas don’t need to be licensed separately as long as they’re passive. The Software Asset Management application considers these secondary replicas as ignored installations. You can view more information about these ignored installations through the Progress indicators widget in the Microsoft publisher overview. For more information on the Microsoft publisher overview, see [Publisher overview for Microsoft in the Software Asset Workspace](../reference/publisher-overview-microsoft.md).

You can use the ServiceNow® Discovery application to automatically locate and identify the Microsoft SQL Server Always On availability groups across your deployment. As part of this discovery process, the application identifies the infrastructure and attributes of each availability group, including the Role \(active or passive replica\), Availability Mode \(synchronous or asynchronous\), Failover Mode \(automatic or manual\), and Readable Secondary \(yes or no\). The Software Asset Management application then uses this information and the applicable licensing rules to calculate your license compliance position for Microsoft SQL Server.

For more information on Microsoft SQL Server licensing, see [Microsoft Per Core licensing rules](microsoft-sw-license-metrics.md). For more information on Always On availability group discovery, see Microsoft SQL Server and Cluster discovery.

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](microsoft-publisher-pack.md)

