---
title: Create service maps
description: Create a service map that maps application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/create-an-app-service-map-kva.html
release: brazil
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enabling application service maps, Configure, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Create service maps

Create a service map that maps application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet.

## Before you begin

You should first enable the Service Maps, by using Istio or Linkerd service meshes or a ServiceNow DaemonSet as part of the Kubernetes Visibility Agent \(KVA\) installation. For more information, see [Enabling application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/enabling-application-service-maps.md).

Role required: discovery\_admin

## About this task

Service maps created using this procedure map application services within a single Kubernetes cluster.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Kubernetes** &gt; **Services** in the navigation filter.

2.  Select **New** and fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |**Name**|Name of the Kubernetes service. If the service does not exist, the service map is created with the default name in the following format: `Name@Namespace@Cluster Name`. You can modify this name.|
    |**Namespace**|Kubernetes namespace that the service belongs to.|
    |**Selector**|Label selector used to identify the pods that the service routes traffic to.|
    |**Kubernetes UID**|Unique identifier assigned to the Kubernetes service by the cluster.|

    If the service for this CI root already exists, the message `Service <service-name> already exists and has the same root CI.` is displayed.

3.  Select **Submit**.

4.  Open the newly created Kubernetes service record.

5.  Select **Create Service Map**.

6.  View the map.

    1.  Select **Open in CMDB Workspace**.

    2.  In the CMDB workspace, select **Open Map**.


## Result

The Service Map is created and is visible in the CMDB workspace.

**Parent Topic:**[Enabling application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/enabling-application-service-maps.md)

