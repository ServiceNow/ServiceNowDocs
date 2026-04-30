---
title: Change the full discovery frequency in Agent Client Collector for Kubernetes – Visibility
description: Customize how often you want the Agent Client Collector for Kubernetes – Visibility Informer to run a full discovery.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, discovery, running, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Agent Client Collector for Kubernetes – Visibility, Configuring Agent Client Collector for Kubernetes – Visibility, Kubernetes discovery using Agent Client Collector for Kubernetes – Visibility, Container discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Change the full discovery frequency in Agent Client Collector for Kubernetes – Visibility

Customize how often you want the Agent Client Collector for Kubernetes – Visibility Informer to run a full discovery.

## Before you begin

Role required: none

## About this task

By default, the Informer runs a full discovery every 24 hours \(1440 minutes\). You can change this frequency by performing the following procedure. For example, change the value to 2880 to make Agent Client Collector for Kubernetes – Visibility run a full discovery every 48 hours \(2880 minutes\).

## Procedure

1.  Do one of the following:

    -   When using a Helm chart: In the Helm install command, add the following command line argument:

        `--set fullDiscoveryMin=<Frequency in minutes>`

    -   When using the k8s\_informer.yaml: Replace the default value with the required one in the line under FULL\_DISCOVERY\_MIN.

