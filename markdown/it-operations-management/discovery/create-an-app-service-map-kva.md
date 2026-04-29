---
title: Create application service maps
description: Create a service map that maps application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enabling application service maps, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Create application service maps

Create a service map that maps application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet.

## Before you begin

Role required: discovery\_admin

You should first enable the application service maps, by using Istio or Linkerd service meshes or a ServiceNow DaemonSet as part of the Kubernetes Visibility Agent \(KVA\) installation. For more information, see [Enabling application service maps](../concept/enabling-application-service-maps.md).

## Procedure

1.  Navigate to **All** and enter `kubernetes service maps` in the navigation filter.

2.  Select the Kubernetes service to use as your entry point for this map.

3.  Select **Create Service Maps**.

    -   If the service does not exist, the service map is created with the default name in the following format: `Name@Namespace@Cluster Name`. You can modify this name.
    -   If the service for this CI root already exists, the message `Service <service-name> already exists and has the same root CI.` is displayed.
    The Service form is opened.

4.  View the map.

    1.  Select **Open in CMDB Workspace**.

    2.  In the CMDB workspace, select **Open Map**.


## Result

The application service map is created and is visible in the CMDB workspace.

**Parent Topic:**[Enabling application service maps](../concept/enabling-application-service-maps.md)

