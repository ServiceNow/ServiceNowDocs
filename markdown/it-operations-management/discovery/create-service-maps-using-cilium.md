---
title: Enable service maps using Cilium
description: Enable application service maps based on the traffic between the workloads in Kubernetes by connecting to a Cilium agent already running in the cluster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/create-service-maps-using-cilium.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 1
keywords: [Cilium, service maps, Kubernetes Visibility Agent, Hubble, connection discovery]
breadcrumb: [Enabling application service maps, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Enable service maps using Cilium

Enable application service maps based on the traffic between the workloads in Kubernetes by connecting to a Cilium agent already running in the cluster.

## Before you begin

Cilium must already be installed and running in the target Kubernetes cluster. ServiceNow does not install Cilium.

This feature is not supported on OpenShift.

Role required: discovery\_admin.

## About this task

Cilium is open-source software that you can run in your Kubernetes cluster to control traffic and apply network policies. If Cilium is already running in the cluster, KVA can connect to the Cilium agent through its Hubble layer to pull traffic data. A DaemonSet pod is deployed with minimal permissions to collect this data and report it to the main Informer pod, which then sends it to the ServiceNow instance.

This method requires fewer permissions than the ServiceNow DaemonSet method and reduces the effort required to get security approval in environments with strict permission policies. The outcomes are the same as the other service map methods. For more information, see [Install Kubernetes Visibility Agent \(KVA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cnov-deploy-install.md).

**Note:** Only the Helm chart installation method is supported for this feature. The `k8s_informer.yaml` file method is not supported.

## Procedure

-   In the Helm `install` command, add the following parameter:

    ```
    --set connectionsDiscovery.method=cilium
    ```


## What to do next

[Create application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-an-app-service-map-kva.md)

**Parent Topic:**[Enabling application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/enabling-application-service-maps.md)

