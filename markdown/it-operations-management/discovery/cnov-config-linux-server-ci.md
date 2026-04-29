---
title: Create a cmdb\_ci\_linux\_server CI for each Kubernetes node
description: Configure if you want the Kubernetes Visibility Agent Informer to create a cmdb\_ci\_linux\_server CI for each Kubernetes node.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, Linux server, CI, CMDB, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\) Informer, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a cmdb\_ci\_linux\_server CI for each Kubernetes node

Configure if you want the Kubernetes Visibility Agent Informer to create a cmdb\_ci\_linux\_server CI for each Kubernetes node.

## Before you begin

Role required: none

## About this task

By default, the Informer creates a cmdb\_ci\_linux\_server CI for every Kubernetes node. If this CI is redundant or interferes with other flows in your organization, you can set the associated configuration parameter to false.

## Procedure

1.  Do one of the following:

    -   When using a Helm chart, in the Helm install command, set the **createServerCi** parameter to false:

        `--set createServerCi=false`

    -   When using the k8s\_informer.yaml file, set the environment variable CREATE\_SERVER\_CI to false.

**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\) Informer](cnov-deploy-install.md)

