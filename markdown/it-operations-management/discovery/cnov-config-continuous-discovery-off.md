---
title: Deactivate continuous discovery in Agent Client Collector for Kubernetes – Visibility
description: Switch off continuous discovery by Agent Client Collector for Kubernetes – Visibility if all you need is periodic snapshots of your cluster resources. If you have multiple clusters with frequent changes, deactivating continuous discovery reduces the load on your instance.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, continuous discovery, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Agent Client Collector for Kubernetes – Visibility, Configuring Agent Client Collector for Kubernetes – Visibility, Kubernetes discovery using Agent Client Collector for Kubernetes – Visibility, Container discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Deactivate continuous discovery in Agent Client Collector for Kubernetes – Visibility

Switch off continuous discovery by Agent Client Collector for Kubernetes – Visibility if all you need is periodic snapshots of your cluster resources. If you have multiple clusters with frequent changes, deactivating continuous discovery reduces the load on your instance.

## Before you begin

Role required: none

## Procedure

1.  Do one of the following:

    -   When using a Helm chart, in the Helm install command, add the following command line argument: `--set continuousDiscovery=false`

    -   When using the k8s\_informer.yaml, enter the value “false” in the line under CONTINUOUS\_DISCOVERY.

