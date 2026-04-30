---
title: Exploring Agent Client Collector for Kubernetes – Visibility
description: Agent Client Collector for Kubernetes – Visibility enables you to gain visibility into on-premises Kubernetes clusters as well as the various Cloud deployments.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-01-15"
reading_time_minutes: 2
keywords: [Agent Client Collector, Kubernetes, Visibility, overview, introduction, benchmark, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Kubernetes discovery using Agent Client Collector for Kubernetes – Visibility, Container discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Exploring Agent Client Collector for Kubernetes – Visibility

Agent Client Collector for Kubernetes – Visibility enables you to gain visibility into on-premises Kubernetes clusters as well as the various Cloud deployments.

Agent Client Collector for Kubernetes – Visibility detects changes on resources in a Kubernetes cluster. It performs continuous discovery, reports any changes back to your instance, and updates the Configuration Management Database \(CMDB\) with the latest data. For the latest information on supported cloud deployments, see the [https://www.servicenow.com/docs/bundle/zurich-it-operations-management/page/product/cloud-native-operations-visibility/reference/cnov-support-matrix.html](https://www.servicenow.com/docs/bundle/zurich-it-operations-management/page/product/cloud-native-operations-visibility/reference/cnov-support-matrix.html) article in the Now Support Knowledge Base.

## How it works

When you deploy Agent Client Collector for Kubernetes – Visibility, Kubernetes creates a Deployment resource in the cluster with the latest data. For the latest information on supported cloud deployments, see the [https://www.servicenow.com/docs/bundle/zurich-it-operations-management/page/product/cloud-native-operations-visibility/reference/cnov-support-matrix.html](https://www.servicenow.com/docs/bundle/zurich-it-operations-management/page/product/cloud-native-operations-visibility/reference/cnov-support-matrix.html) article in the Now Support Knowledge Base. This resource uses a secret stored in Kubernetes to connect to your ServiceNow instance.

The Agent Client Collector for Kubernetes – Visibility Deployment resource contains a pod called Informer, which connects to the Kubernetes API server and receives events on the resources in the cluster from it. The Informer sends the collected data to the instance through the External Communication Channel \(ECC\) Queue table, using the ServiceNow Table API to read from and write to the queue. The Informer then updates the appropriate tables in the CMDB.

**Note:** If the Informer is unable to report the changes, for example due to a network problem, the resources that were added to the cluster during the event are added to the CMDB after the next full discovery cycle. The resources that were removed from the cluster during the event are marked as Absent and deleted after two full discovery cycles.

For more information about the Kubernetes resources on which the Informer collects data and the CMDB tables it populates, see [Data collected by Agent Client Collector for Kubernetes – Visibility](../reference/cnov-collected-data.md).

## Initial and periodic discovery

In its initial discovery, the Informer finds all the resources in the Kubernetes cluster and reports them to your instance. Every 30 seconds, the Informer sends up to 1 MB of data to the instance. It typically takes up to two minutes to report data on a cluster containing 1,000 pods and another minute for every additional 1,000 pods. A single Informer pod can handle a cluster with tens of thousands of pods. If the Informer exits for any reason, Kubernetes restarts it automatically.

After the initial discovery, the Informer continuously monitors the addition, updating, and deletion of resources in the cluster. Resources that were deleted from the cluster are marked with install\_status=Absent and deleted from the CMDB within hours in a regular cleanup.

## Impact of the Informer on the Kubernetes API server

The Informer has minimal impact on the Kubernetes API server. It fetches the complete list of relevant resources only once and saves it to memory. From then on, it synchronizes with the Kubernetes API server and never pulls the complete list again. During the periodic and on-demand full discovery cycles, the Informer resends the saved list of resources to the instance.

## Agent Client Collector for Kubernetes – Visibility performance and scalability benchmark

For Agent Client Collector for Kubernetes – Visibility benchmarks, see the [Performance results for Kubernetes Visibility Agent \[KB1555851\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1555851) article in the Now Support Knowledge Base.

