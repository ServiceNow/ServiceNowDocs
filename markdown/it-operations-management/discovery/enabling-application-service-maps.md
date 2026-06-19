---
title: Enabling application service maps
description: Application service maps give you visibility into how workloads communicate in a Kubernetes cluster, helping you detect dependencies and monitor traffic flows in real time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/enabling-application-service-maps.html
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 2
breadcrumb: [Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Enabling application service maps

Application service maps give you visibility into how workloads communicate in a Kubernetes cluster, helping you detect dependencies and monitor traffic flows in real time.

KVA collects traffic data between workloads and reports it to the ServiceNow instance as part of its installation. Three methods are available: a ServiceNow DaemonSet, Istio or Linkerd service meshes, or Cilium. Each method is suited to different cluster configurations. For deployment prerequisites and installation steps, see [Install Kubernetes Visibility Agent \(KVA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cnov-deploy-install.md).

-   If you use a ServiceNow DaemonSet, a pod runs on each Kubernetes node and reports new connections it detects to the main Informer pod every 60 seconds. To find out how to enable the application service maps using a ServiceNow DaemonSet, see [Enable service maps using DaemonSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-service-maps-using-daemonset.md).
-   If you use service meshes and have a Prometheus server, provide the Prometheus URL. The Informer then queries the Prometheus server periodically for connection data reported by the service mesh. To find out how to enable the application service maps using Istio or Linkerd service meshes, see [Enable service maps using service meshes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-service-maps-using-service-mesh.md).
-   If Cilium is already running in the cluster, the Informer connects to the Cilium agent through its Hubble layer to pull traffic data. A DaemonSet pod is deployed with minimal permissions to collect and report connection data. This method requires fewer permissions than the ServiceNow DaemonSet method. To find out how to enable the application service maps using Cilium, see [Enable service maps using Cilium](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-service-maps-using-cilium.md).

-   **[Enable service maps using DaemonSet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-service-maps-using-daemonset.md)**  
Enable application service maps based on the traffic between the workloads in Kubernetes by using a ServiceNow DaemonSet as part of Kubernetes Visibility Agent \(KVA\) installation.
-   **[Enable service maps using service meshes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-service-maps-using-service-mesh.md)**  
Enable application service maps based on the traffic between the workloads in Kubernetes by using Istio or Linkerd or service meshes as part of Kubernetes Visibility Agent \(KVA\) installation.
-   **[Enable service maps using Cilium](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-service-maps-using-cilium.md)**  
Enable application service maps based on the traffic between the workloads in Kubernetes by connecting to a Cilium agent already running in the cluster.
-   **[Create application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-an-app-service-map-kva.md)**  
Create a service map that maps application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet.
-   **[Create hybrid application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-hybrid-application-service-maps.md)**  
Create hybrid service maps that extend outside the Kubernetes cluster and map other related service resources.

**Parent Topic:**[Configuring Kubernetes Visibility Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cnov-configuring.md)

