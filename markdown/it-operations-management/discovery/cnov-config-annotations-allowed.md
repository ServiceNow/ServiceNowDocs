---
title: Define include and exclude lists of Labels and Annotations
description: In Kubernetes Visibility Agent, define include and exclude lists of Labels and Annotations in Kubernetes resources that the Informer pulls into the Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, labels, annotations, include, exclude, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\) Informer, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Define include and exclude lists of Labels and Annotations

In Kubernetes Visibility Agent, define include and exclude lists of Labels and Annotations in Kubernetes resources that the Informer pulls into the Configuration Management Database \(CMDB\).

## Before you begin

Role required: none

## Procedure

1.  Create an include or exclude list by performing the appropriate procedure.

<table id="choicetable_zc3_nht_51c"><thead><tr><th align="left" id="d400842e90">

Task

</th><th align="left" id="d400842e93">

Procedure

</th></tr></thead><tbody><tr><td id="d400842e99">

**Create an include list**

</td><td>

-   When using a Helm chart, in the Helm install command, add a comma-separated include list of Labels and Annotations.

For example: `--set IncludeLabelsAndAnnotations="label1,label2"`

-   When using the k8s\_informer.yaml file, add values under the environment variable INCLUDE\_LABELS\_AND\_ANNOTATIONS.


</td></tr><tr><td id="d400842e121">

**Create an exclude list**

</td><td>

-   When using a Helm chart, in the Helm install command, add a comma-separated include list of Labels and Annotations.

For example: `--set ExcludeLabelsAndAnnotations="label1,label2"`

-   When using the k8s\_informer.yaml file, add values under the environment variable EXCLUDE\_LABELS\_AND\_ANNOTATIONS.


</td></tr></tbody>
</table>
**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\) Informer](cnov-deploy-install.md)

