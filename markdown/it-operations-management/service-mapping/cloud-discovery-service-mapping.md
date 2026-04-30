---
title: Discovery of application services on cloud using Service Mapping
description: Service Mapping in cloud environments provides critical visibility into application dependencies and connections. By identifying how different application components interact within IaaS and PaaS environments, your organization can gain better insight into its application services and improve overall service management.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-11-06"
reading_time_minutes: 3
keywords: [Service Mapping, Cloud Environments, IaaS, PaaS]
breadcrumb: [Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Discovery of application services on cloud using Service Mapping

Service Mapping in cloud environments provides critical visibility into application dependencies and connections. By identifying how different application components interact within IaaS and PaaS environments, your organization can gain better insight into its application services and improve overall service management.

## IaaS and PaaS environments

To navigate the discovery process effectively, you must first understand the fundamental differences between Infrastructure as a Service \(IaaS\) and Platform as a Service \(PaaS\) environments.

-   **IaaS** - IaaS gives organizations virtual computing resources over the internet, enabling them to manage and deploy their own apps and operating systems. In IaaS, Service Mapping uses a similar discovery process as in private networks, identifying hosts and applications through patterns.
-   **PaaS** - PaaS offers a complete platform for building, launching, and running applications, removing the need for organizations to manage hardware or servers directly. In PaaS, Service Mapping must use cloud platform tools and service accounts to identify devices and applications.

## Performing Discovery in IaaS and PaaS Environments

The discovery process in IaaS environments mirrors that used for private networks.

1.  Locating hosts - Service Mapping starts by using Discovery to locate hosts.
2.  Identifying applications and connections - Patterns are used to identify applications and the connections between those applications and the discovered hosts.
3.  Top-down discovery - Service Mapping performs top-down discovery to map the relationships and connections between devices and applications. It then creates a comprehensive map of the application service.

In contrast to IaaS environments, PaaS environments require a distinct discovery process.

1.  Using cloud platform tools and service accounts - The process begins with a dedicated service account configured for the cloud environment hosting the application service. Service Mapping and Discovery use this service account to access devices and applications. To learn more about setting up an account, see [Set up a cloud service account](../../it-operations-management/concept/setup-cloud-service-account.md).
2.  Horizontal discovery - Discovery performs horizontal discovery in two steps:
    1.  Probes are used to help identify infrastructure devices. See [Horizontal discovery process flow with probes and sensors](../../discovery/concept/c_DiscoProcessFlows.md) for detailed information about the four phases of discovery using probes.
    2.  Patterns help find the applications and services running on those devices. See [Pattern-based discovery in Service Mapping](pattern-based-discovery.md) and [Horizontal discovery process flow with patterns](../../discovery/concept/disco-process-flow-patterns.md) to learn more about discovery using patterns.
3.  Top-down discovery - Service Mapping then performs top-down discovery, creating a comprehensive map of the application service.

## Discovery methods for cloud environments

|Service Mapping/Discovery Approach|IaaS \(Virtual Machines, Servers\)|PaaS \(Functions, Databases, Queues\)|Key requirement difference|
|----------------------------------|----------------------------------|-------------------------------------|--------------------------|
|Top-down service mapping|Supported \(Requires OS credentials or deep agent access\)|Not supported \(or rarely supported\) by cloud metadata discovery alone|Access to the OS layer to trace live connections|
|Tag-based mapping|Supported \(Using collected tags from the cloud resources and containers\)|Supported and highly applicable \(Uses cloud-native tagging/metadata\)|Availability of organized metadata \(tags\)|
|Machine Learning \(ML\)-based mapping|Supported \(Requires capturing running processes and network traffic, thus requires deep discovery\)|Supported, but requires deep discovery \(Only available when using methods that access the underlying OS/container runtime\)|Access to application process data|

Consider an e-commerce application hosted on a cloud provider. In an IaaS environment, Service Mapping identifies virtual machines, databases, and their connections, providing a comprehensive view of the application's infrastructure. In a PaaS environment, it uses cloud platform tools to map application components like managed databases, revealing critical dependencies that impact performance and reliability. This visibility enables better resource management, remediation, and optimization of the application service.

**Parent Topic:**[Exploring Service Mapping](service-mapping-get-started.md)

**Related topics**  


[Discovery for cloud environment](../../discovery/concept/cloud-discovery-wizard.md)

