---
title: Exploring Kubernetes Visibility Agent
description: Kubernetes Visibility Agent enables you to gain visibility into on-premises Kubernetes clusters as well as the various Cloud deployments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/cnov-exploring.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Agent Client Collector, Kubernetes, Visibility, overview, introduction, benchmark, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Exploring Kubernetes Visibility Agent

Kubernetes Visibility Agent enables you to gain visibility into on-premises Kubernetes clusters as well as the various Cloud deployments.

Kubernetes Visibility Agent detects changes on resources in a Kubernetes cluster. It performs continuous discovery, reports any changes back to your instance, and updates the Configuration Management Database \(CMDB\) with the latest data. For the latest information on supported cloud deployments, see the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Support Matrix \[KB1700730\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700730) article in the Now Support Knowledge Base.

## How it works

When you deploy Kubernetes Visibility Agent, Kubernetes creates a Deployment resource in the cluster with the latest data. This resource uses a secret stored in Kubernetes to connect to your ServiceNow instance.

The Kubernetes Visibility Agent Deployment resource contains a pod called Informer, which connects to the Kubernetes API server and receives events on the resources in the cluster from it. The Informer sends the collected data to the instance through the External Communication Channel \(ECC\) Queue table, using the ServiceNow Table API to read from and write to the queue. The backend part of Kubernetes Visibility Agent \(KVA\) then updates the appropriate tables in the CMDB.

**Note:** If the Informer is unable to report the changes, for example due to a network problem, the resources that were added to the cluster during the event are added to the CMDB after the next full discovery cycle. The resources that were removed from the cluster during the event are marked as Absent and deleted after two full discovery cycles.

For more information about the Kubernetes resources on which the Informer collects data and the CMDB tables it populates, see [Data collected by Kubernetes Visibility Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cnov-collected-data.md).

## Initial and periodic discovery

In its initial discovery, the Informer finds all the resources in the Kubernetes cluster and reports them to your instance. Every 30 seconds, the Informer sends up to 1 MB of data to the instance. It typically takes up to two minutes to report data on a cluster containing 1,000 pods and another minute for every additional 1,000 pods. A single Informer pod can handle a cluster with tens of thousands of pods. If the Informer exits for any reason, Kubernetes restarts it automatically.

After the initial discovery, the Informer continuously monitors the addition, updating, and deletion of resources in the cluster. Resources that were deleted from the cluster are marked with install\_status=Absent and deleted from the CMDB within hours in a regular cleanup.

During each full discovery cycle, the system can optionally check for inactive clusters and automatically update their status. When the auto-retirement feature is enabled, clusters that meet specific conditions are retired. A cluster is considered inactive when its associated Informer is in the Down state and the cluster CI has not been touched for a configured period \(default: 60 days\). The system determines this based on the *sys\_updated\_on* field, which indicates when the cluster was last observed by ServiceNow tools, regardless of whether any field values changed. When these conditions are met, the system updates the *install\_status* field on the Kubernetes cluster CI and all associated CIs \(pods, namespaces, deployments, containers, and other resources\). For information about configuring auto-retirement, see [Enable automatic retirement for inactive Kubernetes cluster CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/remove-inactive-cis.md). For details about the configuration properties, see [Kubernetes cluster auto-retirement properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cnov-auto-retire-properties.md).

## Impact of the Informer on the Kubernetes API server

The Informer has minimal impact on the Kubernetes API server. It fetches the complete list of relevant resources only once and saves it to memory. From then on, it synchronizes with the Kubernetes API server and never pulls the complete list again. During the periodic and on-demand full discovery cycles, the Informer resends the saved list of resources to the instance.

## Kubernetes Visibility Agent performance and scalability benchmark

For Kubernetes Visibility Agent benchmarks, see the [Performance results for Kubernetes Visibility Agent \[KB1555851\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1555851) article in the Now Support Knowledge Base.

**Parent Topic:**[Kubernetes Visibility Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/acc-kubernetes-visibility-landing-page.md)

