---
title: Cloud Native Operations release notes
description: Version history for the ITOM Cloud Native Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cloud-native-operations.html
release: store
topic_type: reference
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Cloud Native Operations release notes

Version history for the ITOM Cloud Native Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.3.0 - August 2023**
    -   New features:
        -   New deployment page, including links to recipes for building custom images
        -   Support for automated deployment, without any user intervention
        -   Cluster name taken from cluster context: kubectl get context
        -   Automatic deletion of retired k8s clusters
    -   Ability to improve k8s events and eliminate redundant k8s events already on the agent side
-   **Version 3.1.0 - February 2023**
    -   New:
        -   Cluster name in deployment status table, taken from kubectl
        -   Deployment failure detailed messages, including possible cause and how to fix the issue
    -   Fixed:
        -   Running CNO deployment completes as failed when it was already deployed successfully
        -   Delete is not working for dedicated namespace when the user has multiple namespaces with the same prefix
        -   Delete script from OpenShift/K8S does not delete service/sn-acc-proxy-&lt;instance name&gt; entry
        -   CNO creates false events on Kubernetes nodes in AKS \(Azure Kubernetes Service\)
-   **Version 3.0.0 - November 2022**
    -   The Cloud Native Operations \(CNO\) application provides users with an end-to-end ITOM offering for containerized application services running in Kubernetes or OpenShift clusters, leveraging ServiceNow ITOM existing pipelines and capabilities \(such as Discovery, Event Management, Anomaly Detection, etc\).
    -   Cloud-native apps are designed to run in the elastic and distributed nature required by modern cloud computing platforms, using repeatable automation and orchestration. The uniqueness in this kind of applications is about the nature of ephemeral objects - Pods, deployments, StatefulSets, services, and so on which makes continuous discovery, service mapping and monitoring more dynamic. Existing legacy solutions can't adequately handle cloud-native apps. In addition, we use cloud-native open source technologies \(such as Prometheus and Istio\) which are used extensively in the cloud-native domain.

**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

