---
title: Enable cost allocation in Google Cloud for Kubernetes cluster
description: Enable cost allocation for each Kubernetes cluster before you run a Google Cloud Billing download job to view the Kubernetes spend.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/enable-cost-allocation-kc-gcp.html
release: brazil
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up access to Google Cloud billing and usage data, Configure Cloud Cost Management for Google Cloud, Configure, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Enable cost allocation in Google Cloud for Kubernetes cluster

Enable cost allocation for each Kubernetes cluster before you run a Google Cloud Billing download job to view the Kubernetes spend.

## Before you begin

You should be familiar with Google Cloud policies.

Role required: Google Cloud administrator

## About this task

The steps in this task are performed in the Google Cloud Console. You must enable cost allocation for each Kubernetes cluster in Google Cloud before Cloud Cost Management can attribute Kubernetes spend to the correct resources during billing download. You must enable cost allocation individually for each Kubernetes cluster; enabling it for one cluster doesn't apply to others.

Cloud Cost Management uses tag categories to group related tag names from your cloud provider under a single business-facing label. During billing download, Cloud Cost Management identifies Kubernetes cluster resources using the tag **sn\_ccm\_k8\_cluster\_name**, which is added to resources that already carry Google Cloud's own **goog-k8s-cluster-name** tag. For more information about tag categories, see [Tag categories in Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-cost-management/tag-categories.md).

## Procedure

1.  Log in to the [Google Cloud Console](https://cloud.google.com/cloud-console).

2.  Select the menu icon \[Omitted image "menu-icon.png"\].

3.  Select **Kubernetes Engine**.

4.  Select **Clusters**.

5.  In the Overview section, select a cluster name.

6.  In the Features section, select Cost Allocation.


## Result

The cost allocation for the selected Kubernetes cluster is enabled and you can view the Kubernetes spend.

