---
title: Container image scanning for software decomposition
description: The ITOM Visibility apps, Discovery and Service Mapping Patterns and Kubernetes Visibility Agent integrate with Aqua Trivy to collect data on container images and OS packages. You can increase your control over container deployment by having visibility to the container components.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
keywords: [container, image, Aqua Trivy, security, pattern, scanning, CMDB, Visibility, ACC for Kubernetes - Visibility, Agent Client Collector]
breadcrumb: [Kubernetes discovery using patterns, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Container image scanning for software decomposition

The ITOM Visibility apps, Discovery and Service Mapping Patterns and Kubernetes Visibility Agent integrate with Aqua Trivy to collect data on container images and OS packages. You can increase your control over container deployment by having visibility to the container components.

![Container image scanning for software decomposition diagram](../image/container-image-pattern.png)

## Benefits of image scanning

Scanning your containers gives you visibility into what's inside Kubernetes or Docker containers or OS packages. Scanning images can assist you in multiple ways.

-   It helps you identify software installed in containers for regulatory and compliance use cases.
-   It helps you adhere to company policies like usage of golden images, outdated software, mandatory labels, or configuration policies​.
-   It also helps you manage licensed software running in containers​.
-   You can also get the service context​ by using tags, and service mesh to understand their impact on your organization.

## Image scanning use cases with ITOM Visibility

You can use two ITOM Visibility apps to scan container images, Discovery and Service Mapping Patterns and Kubernetes Visibility Agent. Patterns is a feature set used by Discovery, Cloud Discovery, and Service Mapping. Kubernetes Visibility Agent is a feature of Agent Client Collector. While Kubernetes Visibility Agent \(formerly known as CNO-V\) is more suitable for Kubernetes and dynamic containerized workloads, pattern-based discovery is more suitable for non-Kubernetes Docker containers.

-   **Use case \# 1**

    Once an application has been packaged up in container images, a security professional can scan the base image, as well as the final image, for vulnerabilities, and identify OS packages, software dependencies, and application records. This is specifically for Containerized MSSQL Server.


<table id="table_m1k_b4g_vdc"><thead><tr><th>

Visibility methods

</th><th>

Method characteristics

</th><th>

What's discovered

</th></tr></thead><tbody><tr><td>

Discovery and Service Mapping Patterns and Aqua Trivy:

-   Best suited for self hosted or cloud Kubernetes deployments with access to bearer tokens and credentials.
-   Supports public and self-hosted repository image scanning.

</td><td>

-   Pattern-based discovery without Cloud discovery:
    -   Uses a bearer token.
    -   Manually created Kubernetes discovery schedule per cluster.
-   Pattern-based discovery with Cloud discovery:
    -   No bearer token required.
    -   Uses cloud credentials.
    -   Automatic creation of Kubernetes discovery schedule.
-   For more information on scanning images using Aqua Trivy, see [Scan container images](../task/container-image-task.md).

</td><td>

Discovered using Discovery and Service Mapping Patterns:

 -   Kubernetes clusters
-   Kubernetes Services
-   Kubernetes topology
-   Docker containers and images
-   Kubernetes deployment including OpenShift
-   Namespace
-   Labels and tags
-   Software in containers
-   Account region details can only be discovered by Cloud Discovery
-   Docker Pattern collects data about specific objects in a Docker engine, running on a Linux host

 For more information, see:

-   [Container image discovery](../reference/container_image_scan_pattern.md)
-   [Kubernetes discovery using patterns](kubernetes-discovery.md)
-   [Docker virtualization](../../discovery/concept/c-docker-virtualization.md)

</td></tr><tr><td>

Kubernetes Visibility Agent and Aqua Trivy: -   Best suited for deployment by cloud native app teams.
-   Optional ability to monitor Kubernetes with AIOps.
-   For cloud environments, only AWS ECR \(Public and Private\) is supported.

</td><td>

Kubernetes Visibility Agent -based discovery doesn't require credential set up, and no need for MID Server. Access is through ServiceAccount/ClusterRole. The installation is via Helm Chart or Kubernetes YAML file. The discovery is run near real-time.

 Use Kubernetes Explorer to download SBOM.

</td><td>

Discovered using Kubernetes Visibility Agent

 -   Kubernetes Namespaces
-   Nodes and Pods
-   Deployments
-   Statefulsets
-   Daemonsets
-   Replicasets
-   Jobs
-   Cronjobs
-   Services
-   Docker container
-   Docker image
-   Container repository
-   Account region details can only be discovered by Cloud Discovery

</td></tr></tbody>
</table>-   **Use case \#2**

    A compliance officer can generate an  SBOM  to obtain a detailed list of the dependencies of the container image and to ensure that the software complies with industry regulations.


|Visibility method|Method characteristics|
|-----------------|----------------------|
|Kubernetes pattern or Docker pattern|SBOM creation is part of the container scanning.|
|Kubernetes Visibility Agent|SBOM creation is also a part of the container scanning, but using ACC is best suited for organizations that need flexibility to perform both full and continues discovery.|

-   **Use case \#3**

    An engineer found a defect in a custom-built image and needs to find all Kubernetes pods that are running using that image.


<table id="table_hd4_hqg_vdc"><thead><tr><th>

Visibility method

</th><th>

Method characteristics

</th><th>

What's discovered

</th></tr></thead><tbody><tr><td>

Kubernetes pattern

</td><td>

Aqua Trivy container scanning isn’t required. You can identify the pods using Patterns.

</td><td>

-   Kubernetes Clusters
-   Kubernetes Containers
-   Kubernetes Services
-   Labels
-   Pods
-   Images
-   Tags

</td></tr><tr><td>

Kubernetes pattern with Cloud discovery

</td><td>

Aqua Trivy container scanning isn’t required. You can identify the pods using Patterns.

</td><td>

All the of the above and account or region details

</td></tr></tbody>
</table>-   **Use case \#4**

    An engineer finds a defect in a custom-built image and needs to find all Docker containers \(non Kubernetes\) that are running using that image.


|Visibility method|Method characteristics|What's discovered|
|-----------------|----------------------|-----------------|
|Horizontal Discovery of VM running Docker \(Docker pattern\)|Aqua Trivy container scanning isn’t required. You can identify the pods using Patterns.|See: [Docker virtualization](../../discovery/concept/c-docker-virtualization.md)|

## Image scanning with Discovery and Service Mapping Patterns

Kubernetes and Docker patterns integrate with the Aqua Trivy tool and run scheduled jobs to discover container images and OS packages at fixed intervals of 10 images per minute. During the scan, the pattern indicates the scanning status. The pattern discovers OS packages that are related to an image. Then, it finds the image command attributes like the CI class. Based on the command attributes the pattern creates application records. In addition, the pattern uses enriched scripts to add details to the application records. After that, the pattern maps the relations between the OS packages and the containers.

Part of the data is populated in CMDB tables and part of it in transformation tables \(non-CMDB temporary tables\). The transformation tables are installed with the pattern. For example, the information you get by scanning includes origin registry, software name, and version.

-   **[Link software package information to images only](../task/link-software-package-only-image.md)**  
Link software package information to images rather than containers to avoid empty records that associate to short-lived containers.
-   **[Map MID Server to container image repository](../task/map-mid-server-container-repository.md)**  
If network access or datacenter location requires a specific MID Server, map MID Server to a private container image repository.
-   **[Configure a proxy bypass for specific internal or private container registries](../task/configure-container-proxy-bypass.md)**  
Configure a proxy bypass to allow container image scans to reach specific internal or private registries that require a direct connection.
-   **[Scan container images](../task/container-image-task.md)**  
Enable container image scanning using the Aqua Trivy tool.
-   **[Configure the SBOM generation](../task/enable-sbom.md)**  
Enable the Software Bill of Materials \(SBOM\) creation and avoid duplicate SBOM files from being generated by setting the system properties.
-   **[Download a software bill of materials \(SBOM\)](../reference/generate-sbom-pattern.md)**  
Download a software Bill of Materials \(SBOM\) to gain visibility to the components of the container image such as the operating system packages that are installed.
-   **[Container image discovery](../reference/container_image_scan_pattern.md)**  
The Discovery and Service Mapping Patterns application uses the Scan Container Image pattern to discover Docker images and OS packages data. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Parent Topic:**[Kubernetes discovery using patterns](kubernetes-discovery.md)

**Related topics**  


[Cloud Native Operations for Visibility](../../cloud-native-operations-visibility/concept/cnov-landing.md)

