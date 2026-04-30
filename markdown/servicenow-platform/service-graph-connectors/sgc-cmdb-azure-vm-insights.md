---
title: Enabling VM insights for collecting Azure data
description: You must enable the VM insights feature in the Azure portal for collecting TCP and processes data using the Service Graph Connector for Microsoft Azure.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Additional features, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Enabling VM insights for collecting Azure data

You must enable the VM insights feature in the Azure portal for collecting TCP and processes data using the Service Graph Connector for Microsoft Azure.

## Requirements for enabling the VM insights feature

-   Ensure that you’ve created the Log Analytics workspace to push the logs from virtual machines \(VMs\) via insights in Azure Monitor. See [Insights in Azure Monitor](https://learn.microsoft.com/en-us/azure/azure-monitor/monitor-reference) on the Microsoft Azure documentation site.
-   Note down the subscription name associated with your Log Analytics workspace.

## Collecting the TCP and processes data

The SG-Azure TCP and SG-Azure VM Config Data data sources in the Service Graph Connector for Microsoft Azure import data from the VMConnection and VMProcess tables in Azure, respectively. To fetch data correctly from the VMConnection and VMProcess tables in Azure, you must enable the VM insights feature for all the VMs in your Log Analytics workspace. To learn how to populate these tables via insights, see [Enable VM insights in the Azure portal](https://learn.microsoft.com/en-us/azure/azure-monitor/vm/vminsights-enable-portal) on the Microsoft Azure documentation site.

There are several methods available for enabling VM insights. For more information, see [Enable VM insights overview](https://learn.microsoft.com/en-us/azure/azure-monitor/vm/vminsights-enable-overview) on the Microsoft Azure documentation site.

**Note:** In the data collection rule, ensure that you’ve selected the **Enable guest performance** and **Enable processes and dependencies \(Maps\)** check boxes on the rule form.

