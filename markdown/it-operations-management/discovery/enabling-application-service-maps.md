---
title: Enabling application service maps
description: Service maps map application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet, and sends that information to the ServiceNow instance.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Enabling application service maps

Service maps map application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet, and sends that information to the ServiceNow instance.

Application service maps map the traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet as part of KVA installation. For more information, see [Install Kubernetes Visibility Agent \(KVA\) Informer](../task/cnov-deploy-install.md).

-   If you use a ServiceNow DaemonSet, a pod runs on each Kubernetes node and reports new connections it detects to the main Informer pod every 60 seconds. To find out how to enable the application service maps using a ServiceNow DaemonSet, see [Enable service maps using DaemonSet](../task/create-service-maps-using-daemonset.md).
-   If you use service meshes, have a Prometheus server, and provide the Prometheus URL, the Informer queries the Prometheus server periodically to get information on connections reported by the service mesh. To find out how to enable the application service maps using Istio or Linkerd service meshes, see [Enable service maps using service meshes](../task/create-service-maps-using-service-mesh.md).

-   **[Enable service maps using DaemonSet](../task/create-service-maps-using-daemonset.md)**  
Enable application service maps based on the traffic between the workloads in Kubernetes by using a ServiceNow DaemonSet as part of Kubernetes Visibility Agent \(KVA\) installation.
-   **[Enable service maps using service meshes](../task/create-service-maps-using-service-mesh.md)**  
Enable application service maps based on the traffic between the workloads in Kubernetes by using Istio or Linkerd or service meshes as part of Kubernetes Visibility Agent \(KVA\) installation.
-   **[Create application service maps](../task/create-an-app-service-map-kva.md)**  
Create a service map that maps application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet.
-   **[Create hybrid application service maps](../task/create-hybrid-application-service-maps.md)**  
Create hybrid service maps that extend outside the Kubernetes cluster and map other related service resources.

**Parent Topic:**[Configuring Kubernetes Visibility Agent](cnov-configuring.md)

