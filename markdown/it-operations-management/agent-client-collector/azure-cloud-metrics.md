---
title: Azure cloud metrics
description: Azure cloud metrics are gathered from Azure virtual machines \(VMs\) and Azure storage account policies. Collecting the cloud metrics enables you to monitor the performance of your Azure resources.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# Azure cloud metrics

Azure cloud metrics are gathered from Azure virtual machines \(VMs\) and Azure storage account policies. Collecting the cloud metrics enables you to monitor the performance of your Azure resources.

## Azure cloud metrics collection - Overview

To begin collecting Azure cloud metrics, you must select the metrics that you want to add to the CMDB and set the relevant system configurations. For example, you can monitor the number of bytes sent and received from Azure resources. For details, see [Agent Client Collector for Visibility - Content reference](agent-client-collector-for-visibility-references.md).

## Using Azure policies

You can use preconfigured Azure policies for metric collection, or you can create your own Azure policies.

When using a preconfigured policy, you do the following tasks:

-   Prepare an instance with an active MID Server and metric base.
-   Install Agent Client Collector Framework and Agent Client Collector Monitoring.
-   Run Discovery on the Azure cloud account to populate the CMDB with the configuration items \(CIs\) to be monitored.
-   Configure a proxy agent and assign credentials to the policy. Proxy agents monitor CIs for agents that are in the cloud. Credentials enable the agent to access the Azure policy.

The policies available with the base system for you to activate and configure are described in the following table.

|Policy name|Description|Link to supported metrics|
|-----------|-----------|-------------------------|
|Azure Load Balancer metrics|Collects the metrics for the Azure load balancers.|[Supported metrics for Microsoft Load Balancers](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-network-loadbalancers-metrics)|
|Azure Gateway metrics|Collects the metrics for the Azure network gateway.|[Supported metrics for Microsoft Network Gateways](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-network-natgateways-metrics)|
|Azure Redis Cache metrics|Collects the metrics for the Azure Redis cache.|[Supported metrics for Microsoft Redis cache](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-cache-redis-metrics)|
|Azure Storage Account metrics|Collects the metrics for the Azure storage accounts.|[Supported metrics for Microsoft storage accounts](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-compute-virtualmachines-metrics)|
|Azure Virtual Machine \(VM\) metrics|Collects the metrics for the VMs, which help you monitor Azure VMs.|[Supported metrics for Microsoft virtual machines](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-compute-virtualmachines-metrics)|

## Specifying the CIs for metric collection

When creating policies, you must include the CIs that you want to collect the metrics for in the CMDB. The CIs are typically populated during Discovery, which finds applications and devices on your network and updates the CMDB accordingly.

When creating a policy, you must decide which CIs you want the policy to monitor. To enable monitoring CIs, you do the following tasks:

1.  Configure the Azure Metrics Collector check in the policy.
2.  Set the credentials for the Azure Metrics Collector check to enable retrieving metrics from Azure to the Agent Client Collector agent.
3.  Generate a .json file that specifies the list of resources to be monitored.
4.  Generate a .json file that specifies the list of metrics to be retrieved from monitored resources.

For details on the Azure policies, see [Create Azure policies for metric collection](../task/create-policies-azure.md).

For details on the Azure Metrics Batch API, see the [Metrics Batch API](https://learn.microsoft.com/en-us/rest/api/monitor/metrics-batch/batch?view=rest-monitor-2023-05-01-preview&tabs=HTTP) page.

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](../reference/agent-policies-checks.md)

