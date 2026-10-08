---
title: Create hybrid service maps
description: Create hybrid service maps that extend outside the Kubernetes cluster and map other related service resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/create-hybrid-application-service-maps.html
release: brazil
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enabling application service maps, Configure, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Create hybrid service maps

Create hybrid service maps that extend outside the Kubernetes cluster and map other related service resources.

## About this task

For more information, see [Service Mapping for containerized environments using KVA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/mapping-k8s-sm-kva.md)

## Before you begin

The Kubernetes cluster must be fully discovered using KVA and configured to discover connections between Kubernetes resources. For more information, see [Enabling application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/enabling-application-service-maps.md).

The following must be installed and up-to-date:

-   KVA version 3.14.x or later. See [Prepare for Kubernetes Visibility Agent deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/cnov-deploy-prepare.md).
-   KVA Informer version 2.7.x or later, with the additional settings required for hybrid maps. See [Install Kubernetes Visibility Agent \(KVA\) Informer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/cnov-deploy-install.md).
-   For the latest Helm chart and Kubernetes YAML file release information, see the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Helm Chart and Kubernetes YAML file releases \[KB1564347\]](https://support.servicenow.com/kb?sys_kb_id=4fd37dbe4797f2102c31b98a436d430d&id=kb_article_view) article in the Now Support Knowledge Base.

For Service Mapping prerequisites, including MID Server configuration and required applications, see [Prerequisites for performing top-down discovery using Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/prerequisites-service-mapping.md).

Role required: service\_mapping\_admin

## Procedure

1.  Enable the unified map property.

    For the procedure, see [Access the Unified Map feature from the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping/view-unified-map-sm-workspace.md)

2.  Navigate to **All** and enter `Service mapping` in the navigation filter, in the menu that appears choose **Service Instances**.

3.  Select **New**.

4.  Choose a resource type, choose a resource name, and enter the resource's /URL to use as an entry point for this map.

5.  Select **Create Service Maps**.

6.  View the map.

    1.  Select **Open in CMDB Workspace**.

    2.  In the CMDB workspace, select **Open Map**.


## Result

The hybrid service map is created and is visible in the CMDB workspace.

**Parent Topic:**[Enabling application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/enabling-application-service-maps.md)

