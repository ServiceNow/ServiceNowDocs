---
title: Kubernetes Visibility Agent support matrix
description: The Kubernetes Visibility Agent component is supported on several versions of Kubernetes and OpenShift and in various Kubernetes environments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/cnov-support-matrix.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [OKE, Agent Client Collector, Kubernetes, Visibility, supported, versions, Kubernetes, OpenShift, reference, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Reference, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Kubernetes Visibility Agent support matrix

The Kubernetes Visibility Agent component is supported on several versions of Kubernetes and OpenShift and in various Kubernetes environments.

**Note:** To deploy KVA in the OKE \(Oracle Kubernetes Engine\) environment, you need to create a Kubernetes Cluster on Oracle Cloud Infrastructure. For more information, see the [Oracle](https://www.oracle.com/) documentation.

For the latest information, see the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Support Matrix \[KB1700730\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700730) article in the Now Support Knowledge Base.

## FIPS-140 compliance

FIPS-140 \(Federal Information Processing Standard 140\) is a US government standard for cryptographic modules used in regulated industries. In regulated markets that require FIPS-140 compliant code, the Kubernetes Visibility Agent Informer images have the following FIPS-140 compliance status:

-   The main informer image is FIPS-140 compliant.
-   The daemonset image used for traffic discovery is FIPS-140 compliant.
-   The optional Syft scanner image used for container image scanning is not FIPS-140 compliant.

## Windows nodes

When the **createServerCi** parameter is set to `true`, the Kubernetes Visibility Agent Informer creates a Windows Server \[cmdb\_ci\_win\_server\] CI for each Windows Kubernetes node. To configure server CIs for all node types, see [Configure server CI creation for Kubernetes nodes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/cnov-config-linux-server-ci.md).

-   **[Kubernetes Visibility Agent \(KVA\) Performance Benchmark](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/kva-p-benchmark.md)**  
Performance tests help you estimate the load, memory, and CPU on the Instance and Kubernetes cluster.
-   **[Discovering Kubevirt Virtual Machines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/discover-KVM.md)**  
KubeVirt provides a unified development platform where developers can build, modify, and deploy applications in both Application Containers and Virtual Machines.
-   **[Running Kubernetes Visibility Agent \(KVA\) at Scale](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/running-kva-at-scale.md)**  
When you run Kubernetes Visibility Agent \(KVA\) \(formerly CNO for Visibility\) on more than 100 clusters, configure your system properties to help prevent loss of data from the informers.

**Parent Topic:**[Kubernetes Visibility Agent Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/cnov-reference.md)

