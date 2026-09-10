---
title: Kubernetes explorer dashboard
description: The Discovery Admin Workspace Kubernetes explorer dashboard displays a consolidated view of the Kubernetes resources discovered in your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/kubernetes-explorer-dash.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-08-21"
reading_time_minutes: 5
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Kubernetes explorer dashboard

The Discovery Admin Workspace Kubernetes explorer dashboard displays a consolidated view of the Kubernetes resources discovered in your environment.

To access the dashboard, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Kubernetes Explorer**.

\[Omitted image "daw-kubernetes-ex-dash.png"\] Alt text: DAW Kubernetes explorer dashboard

## Prerequisites

-   **Verify that you have the required setup**
    -   The ServiceNow AI Platform must be running the Brazil, Australia, or the Zurich release starting with Patch 8.
    -   Discovery Admin Workspace must be installed, starting with v1.20.0.
    -   You must have a completed Kubernetes discovery, so that resource data is available to display. For more information, see [Kubernetes discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/kubernetes-discovery.md).

## Required ServiceNow AI Platform roles

The discovery\_admin role is required to view the Kubernetes explorer dashboard.

## Key features

The Kubernetes Explorer dashboard enables you to make data-driven decisions through visualizations. Each tab lists the discovered resources in a table, and most tabs also include visualizations such as data counts, bar charts, and donut charts. From the dashboard, you can do the following:

-   Interact with a visualization to filter the resources in the table on the same tab.
-   Select a resource in a table to open its details page. The details page shows the resource properties and a [Dependency View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-discovery-workspace/dependency-views-map.md) that maps the resource to its related configuration items.
-   Refresh or export the data for a visualization.

-   **Overview tab**

    The **Overview** tab displays a consolidated view of your Kubernetes resources. To refresh or export the data for a visualization, select the **More Options** icon \(\[Omitted image "icon-menu-sow.png"\]\).

    The **Overview** tab includes these data visualizations:

<table id="table_p5d_flw_zjc"><thead><tr><th>

Report title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clusters

</td><td>

Data count and trend line

</td><td>

Kubernetes Cluster Analytics \[sn\_cow\_k8s\_cluster\_analytics\]

</td><td>

Displays the total number and trend of Kubernetes clusters discovered since a given date. Select this report to open the Clusters tab.

</td></tr><tr><td>

Nodes

</td><td>

Data count and trend line

</td><td>

Kubernetes Node Analytics \[sn\_cow\_k8s\_node\_analytics\]

</td><td>

Displays the total number and trend of Kubernetes nodes since a given date.Select this report to open the Nodes tab.

</td></tr><tr><td>

Namespaces

</td><td>

Data count and trend line

</td><td>

Kubernetes Namespace Analytics \[sn\_cow\_k8s\_namespace\_analytics\]

</td><td>

Displays the total number and trend of Kubernetes namespaces discovered since a given date.Select this report to open the Pods tab.

</td></tr><tr><td>

Services

</td><td>

Data count and trend line

</td><td>

Kubernetes Service Analytics \[sn\_cow\_k8s\_service\_analytics\]

</td><td>

Displays the total number and trend of Kubernetes services discovered since a given date.Select this report to open the Services tab.

</td></tr><tr><td>

Pods distribution

</td><td>

Bar chart

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

Displays the distribution of Kubernetes pods, separated by on-premises and cloud infrastructure. Use the Group by list to group the pods by region and data center, geo location, or country.Select a pod in the chart to open the Pods tab.

</td></tr><tr><td>

Kubernetes pods by namespace

</td><td>

Donut chart

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

Displays the distribution of Kubernetes pods grouped by namespace.Select a pod in the chart to open the Pods tab.

</td></tr></tbody>
</table>-   **Clusters tab**

    The **Clusters** tab lists the discovered Kubernetes clusters. The table displays each cluster with its port, provider, and datacenter.

    \[Omitted image "kubernetes-dash-clusters.png"\] Alt text: Clusters tab on the Kubernetes Explorer dashboard

    Select a cluster from the table to open its details page. The details page includes a properties panel, Dependency View, and the Key values, Nodes, and Pods tables.

-   **Services tab**

    The **Services** tab lists the discovered Kubernetes services. A Total services visualization shows the number and trend of services. The Kubernetes services by platform chart groups services by platform or type. Use the Group by list to change the grouping.

    The table displays each service with its service type, Kubernetes cluster, namespace, and IP address. Select a platform or type in the chart to filter the table.

    \[Omitted image "kubernetes-dash-services.png"\] Alt text: Services tab on the Kubernetes Explorer dashboard

    Select a service in the table to open its details page. The details page includes a properties panel, Dependency View, and the Key values table.

-   **Nodes tab**

    The **Nodes** tab displays the discovered Kubernetes nodes. The Nodes by cluster and Nodes by region charts show how nodes are distributed. The table displays each node with its Kubernetes cluster and IP address.

    Select a region in the Nodes by region chart, or a cluster in the Nodes by cluster chart, to filter the Total nodes table.

    \[Omitted image "kubernetes-dash-nodes.png"\] Alt text: Nodes tab on the Kubernetes Explorer dashboard

    Select a node in the table to open its details page. The details page includes a properties panel, Dependency View, and the Key values and Pods tables.

-   **Workloads tab**

    The **Workload** tab lists the discovered Kubernetes workloads. The Total workloads count and the Desired/available replicas mismatch count show workload totals. The Workload by class chart groups workloads by class, such as Kubernetes Deployment, DaemonSet, ReplicaSet, StatefulSet, Cronjob, and Job.

    The table displays each workload with its Kubernetes cluster, namespace, and class. Select a class in the Workload by class chart to filter the table by that class.

    \[Omitted image "kubernetes-dash-workloads.png"\] Alt text: Workloads tab on the Kubernetes Explorer dashboard

    Select a workload in the table to open its details page. The details page includes a properties panel, Dependency View, and the Key values table. The properties in the panel reflect the workload class, such as Kubernetes DaemonSet or Kubernetes StatefulSet.

-   **Pods tab**

    The **Pods** tab lists the discovered Kubernetes pods. Data counts show the total number of pods, and the number of running, pending, creating, and crashloop backoff pods. The table displays each pod with its state, Kubernetes cluster, namespace, owner kind, and IP address.

    Select a count, such as Running pods, to filter the Total pods table.

    \[Omitted image "kubernetes-dash-pods.png"\] Alt text: Pods tab on the Kubernetes Explorer dashboard

    Select a pod in the table to open its details page. The details page includes a properties panel, Dependency View, and the Key values table.

-   **Docker images tab**

    The **Docker images** tab lists the discovered Docker images. The table displays each image with its image ID, operating system, OS family, and OS version.

    \[Omitted image "kubernetes-dash-docker.png"\] Alt text: Docker images tab on the Kubernetes Explorer dashboard

    Select a Docker image in the table to open its details page. The details page includes a properties panel, Dependency View, and the Key values, Container Image OS Packages, Docker Containers, and Pods tables.


