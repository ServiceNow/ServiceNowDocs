---
title: Kubernetes Explorer
description: Use the ServiceNow Kubernetes Explorer to drill-down and view the Kubernetes environments and resources of your organization.
locale: en-US
release: zurich
product: Cloud Discovery Workspace
classification: cloud-discovery-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Cloud Discovery Workspace, ITOM Visibility, IT Operations Management]
---

# Kubernetes Explorer

Use the ServiceNow® Kubernetes Explorer to drill-down and view the Kubernetes environments and resources of your organization.

![Cloud Resources Explorer.](../image/cow-kubernetes-explorer.gif "Kubernetes Explorer")

The Kubernetes Explorer supports the following cloud providers:

-   Amazon Web Services \(AWS\): Amazon Elastic Kubernetes Service \(EKS\)
-   Microsoft Azure Cloud: Azure Kubernetes Service
-   Google Cloud Platform \(GCP\): Google Kubernetes Engine \(GKE\)
-   OpenShift

**Important:** In the Kubernetes Explorer, any Kubernetes resource hosted on OpenShift is considered on-prem. Whereas, any Kubernetes resource hosted on Amazon Web Services \(AWS\), Microsoft Azure, and Google Cloud Platform \(GCP\) is considered cloud hosted.

## Required ServiceNow AI Platform roles

The sn\_cloud\_ops\_ws.cloud\_ops\_admin role is required to view the Kubernetes Explorer.

## Access the Kubernetes Explorer

To open the dashboard, navigate to **All** &gt; **Cloud Discovery Workspace** &gt; **Kubernetes Explorer**.

**Important:** Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_p1d_421_dwb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Application owner

</td><td>

Review the statistics of the applications and workloads running on the Kubernetes clusters.

</td></tr><tr><td>

IT Admin, cloud Admin

</td><td>

-   Review the statistics of the Kubernetes infrastructure: Clusters, Nodes, Namespaces, Services, Pods, and Workloads.
-   Review the distribution of the pods across dimensions such as region/datacenter, geo location, or country.
-   Review the distribution of the pods across namespaces.
-   Review the list of Kubernetes docker images used in your organization.

</td></tr></tbody>
</table>## Indicators

-   **Clusters**

    A Kubernetes cluster is a set of nodes that run containerized applications. The Clusters indicator displays the daily total count and discovery trend of the Kubernetes clusters discovered across the Kubernetes deployments of your organization.

    The Kubernetes Explorer reads the Kubernetes Cluster Analytics \[sn\_cow\_k8s\_cluster\_analytics\] table to compute the Clusters indicator.

-   **Nodes**

    A node is a worker machine in Kubernetes and may be either a virtual or a physical machine, depending on the cluster. The Nodes indicator displays the daily total count and discovery trend of the Kubernetes nodes discovered across the Kubernetes deployments of your organization.

    The Kubernetes Explorer reads the Kubernetes Node Analytics \[sn\_cow\_k8s\_node\_analytics\] table to compute the Nodes indicator.

-   **Namespaces**

    Kubernetes namespaces provides a mechanism for isolating groups of resources within the cluster. The Namespaces indicator displays the daily total count and discovery trend of the Kubernetes namespaces discovered across the Kubernetes deployments of your organization.

    The Kubernetes Explorer reads the Kubernetes Namespace Analytics \[sn\_cow\_k8s\_namespace\_analytics\] table to compute the Namespaces indicator.

-   **Services**

    Kubernetes service is an abstraction which defines a logical set of pods and a policy by which to access them \(sometimes this pattern is called a micro-service\). The Services indicator displays the daily total count and discovery trend of the Kubernetes services discovered across the Kubernetes deployments of your organization.

    The Kubernetes Explorer reads the Kubernetes Service Analytics \[sn\_cow\_k8s\_service\_analytics\] table to compute the Services indicator.

    The Services indicator is also available on the Services tab of the Kubernetes Explorer.


## Breakdowns

-   Pod distribution: This breakdown displays the distribution of Kubernetes pods hosted on the on-prem infrastructure and the cloud infrastructure.

    You can filter the breakdown across the following dimensions:

    -   Region/Datacenter
    -   Geo Location
    -   Country
    The Pod distribution breakdown is available on the Overview tab of the Kubernetes Explorer.

-   Kubernetes services by platform or Kubernetes services by type: This breakdown displays the distribution of Kubernetes services across dimensions such as platform and type.
-   Nodes by region: This breakdown displays the distribution of the Kubernetes nodes across hosting regions.

## Filter

You can filter the list by interacting with the data visualizations such as donut and single score card.

## Data visualizations

<table id="table_mpf_yqw_dwb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kubernetes pods by namespace

</td><td>

Donut![Kubernetes donut icon](../../reporting/image/inline-data-vis-donut.png)

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

This report displays the distribution of Kubernetes pods across the discovered namespaces.This report is available on the Overview tab.

</td></tr><tr><td>

Total clusters

</td><td>

List![Total clusters list icon](../../reporting/image/inline-data-vis-score-list.png)

</td><td>

Kubernetes Cluster Analytics \[sn\_cow\_k8s\_cluster\_analytics\]

</td><td>

This report lists the Kubernetes clusters discovered across the Kubernetes deployments of your organization.This report is available on the Clusters tab. When you click the cluster name, the [Dependency Views map](../../../product/it-operations-management/concept/dependency-views-map.md) appears for Cluster Configuration Item.

</td></tr><tr><td>

Total services

</td><td>

Single score![Total services single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Workload Analytics \[sn\_cow\_k8s\_service\_analytics\]

</td><td>

This report displays the total count of the Kubernetes services.This report is available on the Services tab.

</td></tr><tr><td>

Kubernetes services by platform / type

</td><td>

Donut![Kubernetes services donut icon](../../reporting/image/inline-data-vis-donut.png)

</td><td>

Kubernetes Node Analytics \[sn\_cow\_k8s\_service\_analytics\]

</td><td>

This report displays the distribution of the Kubernetes services across the providers.This report is available on the Services tab.

</td></tr><tr><td>

Kubernetes services

</td><td>

List![Kubernetes services list icon](../../reporting/image/inline-data-vis-score-list.png)

</td><td>

Kubernetes Namespace Analytics \[sn\_cow\_k8s\_service\_analytics\]

</td><td>

This report lists the Kubernetes services discovered.This report is available on the Services tab. When you click the service name, the [Dependency Views map](../../../product/it-operations-management/concept/dependency-views-map.md) appears for Cluster Configuration Item.

</td></tr><tr><td>

Nodes by cluster

</td><td>

Donut![Nodes by cluster donut icon](../../reporting/image/inline-data-vis-donut.png)

</td><td>

Kubernetes Node Analytics \[sn\_cow\_k8s\_node\_analytics\]

</td><td>

This report displays the distribution of the Kubernetes nodes across the discovered clusters.This report is available on the Nodes tab.

</td></tr><tr><td>

Nodes by region

</td><td>

Donut![Nodes by region donut icon](../../reporting/image/inline-data-vis-donut.png)

</td><td>

Kubernetes Node Analytics \[sn\_cow\_k8s\_node\_analytics\]

</td><td>

This report displays the distribution of the Kubernetes nodes across the discovered clusters.This report is available on the Nodes tab.

</td></tr><tr><td>

Total nodes

</td><td>

List![Total nodes list icon](../../reporting/image/inline-data-vis-score-list.png)

</td><td>

Kubernetes Node Analytics \[sn\_cow\_k8s\_node\_analytics\]

</td><td>

This report lists the Kubernetes nodes discovered across the Kubernetes deployments of your organization.This report is available on the Nodes tab. When you click the node name, the [Dependency Views map](../../../product/it-operations-management/concept/dependency-views-map.md) appears for Cluster Configuration Item.

</td></tr><tr><td>

Total workloads

</td><td>

Single score![Total workloads single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Workload Analytics \[sn\_cow\_k8s\_workload\_analytics\]

</td><td>

This report displays the total count of the Kubernetes workloads discovered across the Kubernetes deployments of your organization.This report is available on the Workloads tab.

</td></tr><tr><td>

Desired/available replicas mismatch

</td><td>

Single score![Desired available replicas mismatch single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Workload Analytics \[sn\_cow\_k8s\_workload\_analytics\]

</td><td>

This report displays the count of mismatch between the desired and available replicas.If there's a mismatch, take suitable action to remediate the issue.

</td></tr><tr><td>

Workloads by class

</td><td>

Donut![Workload by class donut icon](../../reporting/image/inline-data-vis-donut.png)

</td><td>

Kubernetes Workload Analytics \[sn\_cow\_k8s\_workload\_analytics\]

</td><td>

This report displays the workloads by the workload class.This report is available on the Workloads tab.

</td></tr><tr><td>

Total workloads

</td><td>

List![Total workloads list icon](../../reporting/image/inline-data-vis-score-list.png)

</td><td>

Kubernetes Workload Analytics \[sn\_cow\_k8s\_workload\_analytics\]

</td><td>

This report lists the Kubernetes workloads discovered across the Kubernetes deployments of your organization.This report is available on the Workloads tab. When you click the workload name, the [Dependency Views map](../../../product/it-operations-management/concept/dependency-views-map.md) appears for Cluster Configuration Item.

</td></tr><tr><td>

Total pods

</td><td>

Single score![Total pods single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

This report displays the total count of Kubernetes pods discovered across the Kubernetes deployments of your organization.This report is available on the Pods tab.

</td></tr><tr><td>

Running pods

</td><td>

Single score![Running pods single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

This report displays the total count of the Kubernetes pods that are in running state.This report is available on the Pods tab.

</td></tr><tr><td>

Pending pods

</td><td>

Single score![Pending pods single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

This report displays the total count of the Kubernetes pods that are in pending state.This report is available on the Pods tab.

</td></tr><tr><td>

Creating pods

</td><td>

Single score![Creating pods single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

This report displays the total count of the Kubernetes pods that are in the creating state.This report is available on the Pods tab.

</td></tr><tr><td>

Crashloop backoff pods

</td><td>

Single score![Crashloop backoff single score icon](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

This report displays the total count of the Kubernetes pods that are in the crashloop backoff state.This report is available on the Pods tab.

</td></tr><tr><td>

Total pods

</td><td>

List![Total pods list icon](../../reporting/image/inline-data-vis-score-list.png)

</td><td>

Kubernetes Pod Analytics \[sn\_cow\_k8s\_pod\_analytics\]

</td><td>

This report lists the Kubernetes pods discovered across the Kubernetes deployments of your organization.This report is available on the Pods tab. When you click the pod name, the [Dependency Views map](../../../product/it-operations-management/concept/dependency-views-map.md) appears for Cluster Configuration Item.

</td></tr><tr><td>

Docker images

</td><td>

List![Docker images list icon](../../reporting/image/inline-data-vis-score-list.png)

</td><td>

Kubernetes Image Analytics \[sn\_cow\_k8s\_img\_analytics\]

</td><td>

This report lists the Docker images discovered across the Kubernetes deployments of your organization.This report is available on the Docker images tab. When you click the doker image name, the [Dependency Views map](../../../product/it-operations-management/concept/dependency-views-map.md) appears for Cluster Configuration Item. You can download the SBOM. To generate the SBOM, see [Download a software bill of materials \(SBOM\)](../../../product/service-mapping/reference/generate-sbom-pattern.md).

</td></tr></tbody>
</table>