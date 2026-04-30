---
title: Add custom Labels and Annotations to Kubernetes resources
description: Add custom Labels and Annotations to all resources deployed by Kubernetes Visibility Agent in the Kubernetes cluster.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, labels, annotations, custom, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\), Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Add custom Labels and Annotations to Kubernetes resources

Add custom Labels and Annotations to all resources deployed by Kubernetes Visibility Agent in the Kubernetes cluster.

## Before you begin

Role required: none

## Procedure

1.  Do one of the following:

    -   When using a Helm chart, in the Helm install command, add the custom attributes to the values.yaml file.

        Use the format shown in this example:

        `--set commonLabels.mylabel1=value1 --set commonLabels.mylabel2=value2 --set commonAnnotations.myannotation1=value3`.

    -   When using the k8s\_informer.yaml file, add custom Labels and Annotations manually to the relevant resources in the file.
    **Note:**

    Label and Annotation names must be alphanumeric and contain no spaces or special characters. For limitations on Label values, see the [Kubernetes documentation](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/#syntax-and-character-set).


**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\)](cnov-deploy-install.md)

