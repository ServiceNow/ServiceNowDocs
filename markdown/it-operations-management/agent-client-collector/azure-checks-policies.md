---
title: Azure Health Monitoring default checks and policies
description: Agent Client Collector provides the following default checks and policies for Azure health monitoring.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Azure Health Monitoring default checks and policies

Agent Client Collector provides the following default checks and policies for Azure health monitoring.

<table id="table_snq_v3n_trb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

azure.metrics-k8s-service

</td><td>

Provides pod, nodes, and cluster level metrics from all Azure Kubernetes services in metric form.Usage: metrics-azure-k8s-service.rb

```
-S, --subscription ID ARM Subscription ID
-r, Region
```

Example: `metrics-azure-k8s-service.rb -S {{.labels.params_subscription_id}} -r westus2`

</td><td>

`metrics-azure-k8s-service.rb -r {{.labels.params_ci_region}} {{-s {{if.labels.params_subscription_id}} -S {{.labels.params_subscription_id}} {{end}}`

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

