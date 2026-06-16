---
title: Kubernetes Visibility Agent release notes
description: Version history for the Kubernetes Visibility Agent application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-kubernetes-visibility-agent.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Kubernetes Visibility Agent release notes

Version history for the Kubernetes Visibility Agent application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.15.0 - June 2026**
    -   New:
        -   Integrated Cilium with KVA to retrieve Kubernetes resource connectivity data for creating service maps
        -   Added the ability to automatically retire Kubernetes clusters and related resources when no activity is detected within a configurable time period
    -   Changed: Updated KVA licensing to an image-based model, replacing the previous container-based approach
-   **Version 3.14.1 - March 2026**
    -   Informer Version 2.7.1 - \[March 2026 Store Release\]:
        -   New:
            -   Service maps now include Kubernetes and all related service resources beyond the Kubernetes environment.
            -   Kubernetes Service Maps offer more control over the CI visualization.
            -   KubeVirt VMs running in Kubernetes are being now added to the CMDB.
            -   Service mapping with KVA for micro-services is supported.
            -   KVA pod can run in an OKE \(Oracle Kubernetes Engine\) environment.
    -   Fixed: KVA now populates ObjectID in alignment with SGC for EKS, AKS and GKE cluster environments.
-   **Version 3.13.0 - December 2025**
    -   New: Additional control over the CIs displayed in Kubernetes Service MapsBring KubeVirt VMs running in Kubernetes into the CMDB
    -   Changed: Option to force TLS 1.3 connection between Informer and SN instanceDiscover External IP addresses of K8s Service using helm flag
-   **Version 3.11.0 - August 2025**
    -   Informer Version 2.5.0
        -   New:
            -   New Service Mapping feature.
            -   Enhancement of complex filter logic for config map
            -   CI deletion strategy for namespace CI
            -   optional liveness and health probe support.
    -   Informer Version 2.4.0
        -   New:
            -   GCP secrets support for Storing the ServiceNow instance credentials.
            -   Support for custom root certificate authority while Informer connects to the instance.
-   **Version 3.10.2 - March 2025**

    Kubernetes Visibility Agent offers cutting-edge monitoring for Kubernetes resources, performing continuous discovery and promptly reporting changes. It keeps your Configuration Management Database \(CMDB\) up to date with the latest data for optimal accuracy. Upon deployment, KVA sets up a Deployment resource in your cluster, featuring anInformer pod. This pod connects to the Kubernetes API server, efficiently receiving and processing resource events. Achieve unparalleled visibility into your on-premises Kubernetes clusters and cloud deployments, including Amazon EKS, Google GKE, Azure AKS, Red Hat OpenShift, and Rancher. Enhance your resource management and operational efficiency with Kubernetes Visibility Agent.


