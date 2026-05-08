---
title: View your cluster setup in 360 degrees
description: Get a 360-degree perspective of your cluster setup to manage license consumption across the cluster.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View your cluster setup in 360 degrees

Get a 360-degree perspective of your cluster setup to manage license consumption across the cluster.

## Before you begin

Role required: sam\_admin

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License usage**.

2.  Select a publisher card to open the publisher details page.

3.  From the Publisher details page, select a software model from the navigation tree on the left hand side.

4.  From the **License Metrics Results** tab, select the value on the **Licenses required** column.

5.  In the Licenses Required By page, select a cluster from the **Cluster** column.

    The cluster record page opens.

6.  Select **SAM Cluster 360°**.

    The cluster setup appears.

7.  View the following details on the cluster.

    -   Infrastructure: View entities such as hosts, virtual machines \(VMs\), host affinity rules, and software installations in the cluster. Select an entity to view the complete list. For example, select **Software Installs** to view all software installations. You can group the software installations by normalized publisher, normalized product, or by software model results. You can also select any software installation from the list such as SQL Server to view all SQL Server software installations in that cluster.
    -   Licensing details: View the software models consuming licenses, allocations, device license consumption analysis, and ignored installations on the cluster. Select an entity to view the complete list.
    -   Health issues: View all health issues across products in the cluster. Additionally, view installations that require your attention to be considered for reconciliation.
    The 360-degree view lets you drill down from the top view of an entity to the lowest level to better understand license composition and remediation actions across the cluster. As an example, you can select a software model to drill down to view its metric attributes, override license costs, downgrade rights, software entitlements, and software model results. You can further select any of these entities, such as software model results, to get to its lowest denominator.

8.  Select **Open Dependency View** to view the relationship between the nodes of the cluster.

    For details on Dependency Views, see Dependency Views map menus and controls.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

