---
title: Configure server CI creation for Kubernetes nodes
description: Configure whether the Kubernetes Visibility Agent Informer creates a server CI for each Kubernetes node.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/cnov-config-linux-server-ci.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, Linux server, Windows server, CI, CMDB, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\) Informer, Configure, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure server CI creation for Kubernetes nodes

Configure whether the Kubernetes Visibility Agent Informer creates a server CI for each Kubernetes node.

## Before you begin

Role required: none

## About this task

By default, the Informer creates a server CI for every Kubernetes node: a Linux Server \[cmdb\_ci\_linux\_server\] CI for each Linux node and a Windows Server \[cmdb\_ci\_win\_server\] CI for each Windows node. Both CI types have the same fields populated. If a matching virtual machine was already discovered, for example by Cloud Discovery or a Service Graph connector, the Informer relates the server CI to the VM Instance \[cmdb\_ci\_vm\_instance\] CI. If these CIs are redundant or interfere with other flows in your organization, you can set the associated configuration parameter to false.

**Note:** The Informer doesn't create a server CI for a node that represents an AWS Fargate profile in an Amazon EKS cluster.

## Procedure

1.  Do one of the following:

    -   When using a Helm chart, in the Helm install command, set the **createServerCi** parameter to false:

        `--set createServerCi=false`

    -   When using the k8s\_informer.yaml file, set the environment variable CREATE\_SERVER\_CI to false.

**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\) Informer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/cnov-deploy-install.md)

