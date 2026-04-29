---
title: Enable cost allocation in Google Cloud for Kubernetes cluster
description: Enable cost allocation for each Kubernetes cluster before you run a Google Cloud Billing download job to view the Kubernetes spend.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up access to Google Cloud billing and usage data, Configure Cloud Cost Management for Google Cloud, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Enable cost allocation in Google Cloud for Kubernetes cluster

Enable cost allocation for each Kubernetes cluster before you run a Google Cloud Billing download job to view the Kubernetes spend.

## Before you begin

Role required: Google Cloud administrator

-   You should be familiar with Google Cloud policies.
-   Install Discovery and Service Mapping Patterns application \(sn\_itom\_pattern\) 1.10.2 or higher. For more information, see [Install Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=install-discovery-service-mapping-patterns&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   Install CMDB CI Class Models \(sn\_cmdb\_ci\_class\) version 1.53.1 or higher. For more information, see [CMDB CI Class Models app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   To set up Kubernetes discovery, see [Kubernetes discovery using patterns](https://www.servicenow.com/docs/access?context=kubernetes-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

## About this task

-   For identifying resources for Kubernetes clusters during billing download, the tag **sn\_ccm\_k8\_cluster\_name** is added to the resources, which already have **goog-k8s-cluster-name** tags.
-   You must enable cost allocation for each individual Kubernetes cluster.

## Procedure

1.  Log in to the [Google Cloud Console](https://cloud.google.com/cloud-console).

2.  Select the menu icon ![Menu icon.](../image/menu-icon.png).

3.  Select **Kubernetes Engine**.

4.  Select **Clusters**.

5.  In the Overview section, select a cluster name.

6.  In the Features section, select Cost Allocation.


## Result

The cost allocation for the selected Kubernetes cluster is enabled and you can view the Kubernetes spend.

