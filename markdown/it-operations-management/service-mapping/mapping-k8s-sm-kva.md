---
title: Service Mapping for containerized environments using KVA
description: Kubernetes Visibility Agent \(KVA\) and Service Mapping discover and visualize application dependencies across Kubernetes clusters and related resources, providing complete visibility into containerized environments.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-02-16"
reading_time_minutes: 2
keywords: [Service Mapping, Kubernetes, hybrid environments, container discovery, application dependencies, topology-mapping, cloud native]
breadcrumb: [Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping for containerized environments using KVA

Kubernetes Visibility Agent \(KVA\) and Service Mapping discover and visualize application dependencies across Kubernetes clusters and related resources, providing complete visibility into containerized environments.

Service Mapping for containerized environments provides automated discovery and visualization of application dependencies across your entire technology stack. Whether your applications run entirely within Kubernetes clusters or span multiple environments including cloud databases, API gateways, and traditional servers, Service Mapping creates comprehensive topology maps that show how services connect and depend on each other.

Service Mapping and KVA combined capabilities transform complex architectures into clear, actionable service maps that help teams troubleshoot faster, assess change impact more accurately, and optimize application performance across environments.

## Key capabilities

-   **Seamless entry point discovery and mapping**

    Start with any application endpoint such as a URL or hostname and port, and Service Mapping automatically identifies the corresponding Kubernetes resource serving that endpoint. KVA recognizes multiple Kubernetes exposure methods including load balancers, ingress controllers, NodePort services, Gateway API resources, and OpenShift routes.

-   **Complete Kubernetes topology-mapping**

    Discover and visualize traffic flows between pods within your Kubernetes clusters. Service maps display workloads including deployments, stateful sets, daemon sets, jobs, and cron jobs. You can choose to view either workloads or Kubernetes services on your maps, providing flexibility in how you analyze your container infrastructure.

-   **External dependency tracking**

    Automatically detect connections from Kubernetes pods to external resources including cloud databases, third-party APIs, and traditional infrastructure. KVA resolves DNS connections and Kubernetes ExternalName services to be able to map dependencies beyond cluster boundaries.

-   **Bidirectional discovery**

    Service maps work regardless of whether your entry point leads directly to a Kubernetes resource or to an external component with downstream connections into clusters. This flexibility promotes comprehensive visibility across any architecture.


## Use Cases

-   **Accelerated incident resolution**

    When incidents occur, Service Mapping provides immediate visibility into all dependencies, helping teams quickly identify root causes and understand the impact across Kubernetes and traditional infrastructure.

-   **Change impact analysis**

    Before changing Kubernetes deployments, APIs, or infrastructure components, visualize all upstream and downstream dependencies to understand potential impacts and plan maintenance accordingly.

-   **Application rationalization**

    Gain complete visibility into which services support critical business applications, enabling data-driven decisions, resource allocation, and technical debt reduction.


## Benefits

-   Reduced mean time to resolution through comprehensive visibility into service architectures
-   Minimized risk from changes by reviewing dependencies before modifying Kubernetes or infrastructure components
-   Improved operational efficiency by automating discovery instead of manually documenting complex service relationships
-   Better decision-making through accurate, up-to-date topology information that reflects actual application behavior
-   Simplified compliance and audit processes with automated documentation of service dependencies and data flows

## Getting Started

To begin discovering and mapping Kubernetes services, install Kubernetes Visibility Agent \(KVA\) latest version and make sure Service Mapping requirements are met. For more information, see:

-   [Configuring Kubernetes Visibility Agent](../../cloud-native-operations-visibility/concept/cnov-configuring.md)
-   [Configuring Service Mapping](service-mapping-setup.md)

[Create hybrid application service maps](../../cloud-native-operations-visibility/task/create-hybrid-application-service-maps.md)

Enter an application entry point into Service Mapping. KVA automatically identifies whether this entry point connects to Kubernetes resources and initiates comprehensive topology discovery.

