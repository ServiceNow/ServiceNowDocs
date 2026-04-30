---
title: Deactivate continuous discovery in Kubernetes Visibility Agent
description: Switch off continuous discovery by Kubernetes Visibility Agent if all you need is periodic snapshots of your cluster resources. If you have multiple clusters with frequent changes, deactivating continuous discovery reduces the load on your instance.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, continuous discovery, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\), Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Deactivate continuous discovery in Kubernetes Visibility Agent

Switch off continuous discovery by Kubernetes Visibility Agent if all you need is periodic snapshots of your cluster resources. If you have multiple clusters with frequent changes, deactivating continuous discovery reduces the load on your instance.

## Before you begin

Role required: none

## Procedure

1.  Do one of the following:

    -   When using a Helm chart, in the Helm install command, add the following command line argument: `--set continuousDiscovery=false`

    -   When using the k8s\_informer.yaml, enter the value “false” in the line under CONTINUOUS\_DISCOVERY.

**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\)](cnov-deploy-install.md)

