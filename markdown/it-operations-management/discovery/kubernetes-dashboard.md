---
title: Kubernetes dashboard
description: Use the Kubernetes dashboard to review the statistics for the Kubernetes platform used by your organization.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Discovery Platform Analytics Solutions, Discovery, ITOM Visibility, IT Operations Management]
---

# Kubernetes dashboard

Use the Kubernetes dashboard to review the statistics for the Kubernetes platform used by your organization.

## Required ServiceNow AI Platform roles

service\_mapping\_admin, service\_mapping\_user, sn\_k8s.cno\_admin

## Access the Assessment dashboard

To open the dashboard, navigate to **All** &gt; **** &gt; **Cloud Native Operations** &gt; **Discovery Dashboard**.

Alternatively, navigate to **All** &gt; **Configuration** &gt; **Kubernetes**.

After upgrading to Discovery Admin Workspace version 1.3.1 \(August 2024 Store\), you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the enhanced dashboard.

![Kubernetes dashboard](../image/kubernetes-dashboard.png "Kubernetes dashboard")

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|Application owner|Review the statistics of the applications and workloads running on the Kubernetes clusters.|
|IT admin, cloud admin|Review the statistics of the Kubernetes infrastructure: namespaces, nodes, clusters.|

## Indicators

-   **Kubernetes Clusters**

    Number of discovered Kubernetes clusters.

-   **Kubernetes Namespaces**

    Number of discovered Kubernetes namespaces.

-   **Kubernetes Nodes**

    Number of discovered Kubernetes nodes.

-   **Kubernetes Pods**

    Number of discovered Kubernetes Pods.


## Data visualizations

The following visualizations are available on the Overview tab of Cloud Migration Assessment.

<table id="table_lcd_5vt_yrb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kubernetes Workloads

</td><td>

Pie![](../../reporting/image/icon-pie-report-p.png)

</td><td>

Kubernetes Namespace \[cmdb\_ci\_kubernetes\_workloads\]

</td><td>

A pie chart report that presents the statistics on discovered Kubernetes workloads.

</td></tr><tr><td>

Kubernetes Pods

</td><td>

Pie![](../../reporting/image/icon-pie-report-p.png)

</td><td>

Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]

</td><td>

A pie chart report that presents the statistics discovered Kubernetes pods in the Kubernetes platform.

</td></tr></tbody>
</table>