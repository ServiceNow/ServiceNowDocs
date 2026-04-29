---
title: Change the full discovery frequency in Kubernetes Visibility Agent
description: Customize how often you want the Kubernetes Visibility Agent Informer to run a full discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, discovery, running, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\) Informer, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Change the full discovery frequency in Kubernetes Visibility Agent

Customize how often you want the Kubernetes Visibility Agent Informer to run a full discovery.

## Before you begin

Role required: none

## About this task

By default, the Informer runs a full discovery every 24 hours \(1440 minutes\). You can change this frequency by performing the following procedure. For example, change the value to 2880 to make Kubernetes Visibility Agent run a full discovery every 48 hours \(2880 minutes\).

## Procedure

1.  Do one of the following:

    -   When using a Helm chart: In the Helm install command, add the following command line argument:

        `--set fullDiscoveryMin=<Frequency in minutes>`

    -   When using the k8s\_informer.yaml: Replace the default value with the required one in the line under FULL\_DISCOVERY\_MIN.

**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\) Informer](cnov-deploy-install.md)

