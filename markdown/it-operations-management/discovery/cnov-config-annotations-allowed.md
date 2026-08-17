---
title: Define include and exclude lists of Labels and Annotations
description: In Kubernetes Visibility Agent, define include and exclude lists of Labels and Annotations in Kubernetes resources that the Informer pulls into the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/cnov-config-annotations-allowed.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, labels, annotations, include, exclude, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\) Informer, Configure, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Define include and exclude lists of Labels and Annotations

In Kubernetes Visibility Agent, define include and exclude lists of Labels and Annotations in Kubernetes resources that the Informer pulls into the Configuration Management Database \(CMDB\).

## Before you begin

Role required: none

## About this task

By default, that is if **includeLabelsAndAnnotations** and **excludeLabelsAndAnnotations** aren't set, the KVA discovers and includes all the available Kubernetes labels and annotations on the supported Kubernetes resource.

Empty label and annotation values and values longer than 255 characters aren't sent to the CMDB. Duplicate key and value pairs for the same CI are also ignored.

-   Use **includeLabelsAndAnnotations** when you want to restrict discovery to a specific list of label or annotation keys.
-   Use **excludeLabelsAndAnnotations** when you want to prevent specific label or annotation keys from being sent to the CMDB.

If both options are configured, **excludeLabelsAndAnnotations** takes precedence. If the same key appears in both lists, the key is excluded and is not sent to the CMDB.

## Procedure

1.  Create an include or exclude list by using the following procedure.

<table id="choicetable_zc3_nht_51c"><thead><tr><th align="left" id="d416933e139">

Task

</th><th align="left" id="d416933e142">

Procedure

</th></tr></thead><tbody><tr><td id="d416933e148">

**Create an include list**

</td><td>

-   When using a Helm chart, in the Helm install command, add a comma-separated include list of Labels and Annotations.

For example: `--set IncludeLabelsAndAnnotations="label1,label2"`

-   When using the k8s\_informer.yaml file, add values under the environment variable INCLUDE\_LABELS\_AND\_ANNOTATIONS.


</td></tr><tr><td id="d416933e170">

**Create an exclude list**

</td><td>

-   When using a Helm chart, in the Helm install command, add a comma-separated exclude list of Labels and Annotations.

For example: `--set ExcludeLabelsAndAnnotations="label1,label2"`

-   When using the k8s\_informer.yaml file, add values under the environment variable EXCLUDE\_LABELS\_AND\_ANNOTATIONS.


</td></tr></tbody>
</table>
**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\) Informer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cnov-deploy-install.md)

