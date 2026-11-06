---
title: Kubernetes Visibility Agent \(KVA\) release notes
description: The ServiceNow Kubernetes Visibility Agent \(KVA\) provides comprehensive discovery and monitoring of Kubernetes resources in your environment. See the following sections for release notes by version.Kubernetes Visibility Agent \(KVA\) enhances container and cluster monitoring with improved resource discovery and expanded dashboard capabilities. These updates help administrators maintain comprehensive visibility into Kubernetes environments and support better service mapping.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/kubernetes-visibility-agent-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Kubernetes, Kubernetes Visibility, ITOM Visibility, Discovery, Kubernetes, Kubernetes Visibility, ITOM Visibility, Discovery]
breadcrumb: [ITOM Visibility release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Kubernetes Visibility Agent \(KVA\) release notes

The ServiceNow® Kubernetes Visibility Agent \(KVA\) provides comprehensive discovery and monitoring of Kubernetes resources in your environment. See the following sections for release notes by version.

## About Kubernetes Visibility Agent \(KVA\)

-   Discover and monitor Kubernetes clusters, nodes, namespaces, services, workloads, pods, and Docker images automatically.
-   Visualize Kubernetes resource relationships and dependencies through integrated dashboards and dependency views.
-   Maintain an up-to-date inventory of containerized applications and infrastructure to support service mapping and incident management.

See [ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-visibility-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Kubernetes Visibility Agent \(KVA\) is available as a store application. Install the application from the ServiceNow Store and configure the agent to connect to your Kubernetes clusters.

-   **Upgrade information**

    Upgrade to the latest version through the ServiceNow Store. After upgrading the application, update the Kubernetes Visibility Agent \(KVA\) deployment in your clusters to the corresponding version.

-   **Browser requirements**

    Use the latest version of Chrome, Firefox, Safari, or Edge for optimal performance when accessing the Kubernetes explorer dashboard.

-   **Additional requirements**

    Requires ITOM Visibility base plugins, Discovery, and appropriate Kubernetes cluster access permissions. The agent must be deployed in each Kubernetes cluster you want to monitor.


## Accessibility and localization

-   **Accessibility information**
    -   The Kubernetes explorer dashboard is navigable by keyboard and compatible with screen readers including JAWS and NVDA.
-   **Localization information**

    This application is available in English. Additional language support may be added in future releases.


**Parent Topic:**[ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-visibility-rn.md)

## Version 3.16.1

Kubernetes Visibility Agent \(KVA\) enhances container and cluster monitoring with improved resource discovery and expanded dashboard capabilities. These updates help administrators maintain comprehensive visibility into Kubernetes environments and support better service mapping.

### What's new

-   **Software decomposition tool using Syft Scanner**

    Analyze container images and generate Software Bill of Materials \(SBOM\) using the integrated Syft Scanner. The new software decomposition tool helps administrators identify software components, dependencies, and vulnerabilities within containerized applications, supporting security compliance and risk management.

-   **FIPS 140 compliance**

    Deploy Kubernetes Visibility Agent \(KVA\) with FIPS 140 compliant main informer and daemonset images. These images meet federal security standards for cryptographic modules, enabling deployment in regulated environments that require FIPS 140 compliance.


### What's changed

-   **Kubernetes resource dependency views**

    Resource details pages now include enhanced Dependency Views that show relationships between Kubernetes resources and related configuration items. The improved visualization helps administrators understand service dependencies and troubleshoot issues more effectively.


### What's deprecated or removed

-   **Legacy Kubernetes discovery API**

    The legacy Kubernetes discovery API is deprecated and will be removed in a future release. Use the enhanced discovery capabilities and updated API endpoints introduced in this release.


