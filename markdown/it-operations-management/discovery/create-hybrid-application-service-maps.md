---
title: Create hybrid application service maps
description: Create hybrid service maps that extend outside the Kubernetes cluster and map other related service resources.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enabling application service maps, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Create hybrid application service maps

Create hybrid service maps that extend outside the Kubernetes cluster and map other related service resources.

## About this task

... For more information, see [Service Mapping for containerized environments using KVA](../../service-mapping/concept/mapping-k8s-sm-kva.md)

## Before you begin

Role required: service\_mapping\_admin

Using hybrid service mapping to include both Kubernetes and non-Kubernetes application services requires additional settings, special prerequisites, and a different procedure.

Refer to [Configuring Service Mapping](../../service-mapping/concept/service-mapping-setup.md) for more information about service mapping.

The following applications must be installed and up-to-date:

-   KVA version 3.14.x or later, see [Prepare for Kubernetes Visibility Agent deployment](cnov-deploy-prepare.md)
-   KVA Informer version 2.7.x or later. See [Install Kubernetes Visibility Agent \(KVA\)](cnov-deploy-install.md) for additional settings required for the Hybrid maps.
-   Service Mapping. For more information, see [Request Service Mapping](../../service-mapping/task/t_ActivateServiceMappingPlugin.md).
-   Discovery and Service Mapping Patterns version 1.30.x or later \(March 2026 version\)
-   MID Server. See [MID server configuration for Service Mapping](../../service-mapping/concept/configure-mid-service-mapping.md). Verify that you have at least one MID Server configured with the Service Mapping application and with an IP range that covers the address 192.168.0.1. See [MID Server configuration for Service Mapping](../../service-mapping/concept/configure-mid-service-mapping.md).
-   For the latest information on Helm chart and Kubernetes YAML file releases, see the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Helm Chart and Kubernetes YAML file releases \[KB1564347\]](https://support.servicenow.com/kb?sys_kb_id=4fd37dbe4797f2102c31b98a436d430d&id=kb_article_view) article in the Now Support Knowledge Base.

For more information on Service mapping prerequisites, see [Prerequisites for performing top-down discovery using Service Mapping](../../service-mapping/reference/prerequisites-service-mapping.md)

Before creating a service map, verify that the Kubernetes cluster was fully discovered using KVA and that it's configured to discover connections between Kubernetes resources. In other words, enable KVA service maps as shown in [Enabling Application Service Maps](../concept/enabling-application-service-maps.md).

For the service mapping procedure, see [Map a single application service using classic Service Mapping](../../service-mapping/task/t_DefineNewBusinessService.md)

## Procedure

1.  Enable the hybrid map property on the System Properties table \(**All** &gt; **System Properties** &gt; **All Properties**\).

    1.  Locate the **sa.sm\_scoped\_app.sa.unified\_map** property.

    2.  Set the property value to **enabled**.

2.  Navigate to **All** and enter `Service mapping` in the navigation filter, in the menu that appears choose Service Instances.

3.  Select **New**.

4.  Choose a resource type, choose a resource name, and enter the resource's /URL to use as an entry point for this map.

5.  Select **Create Service Maps**.

6.  View the map.

    1.  Select **Open in CMDB Workspace**.

    2.  In the CMDB workspace, select **Open Map**.


## Result

The hybrid application service map is created and is visible in the CMDB workspace.

**Parent Topic:**[Enabling application service maps](../concept/enabling-application-service-maps.md)

