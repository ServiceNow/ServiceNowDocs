---
title: Monitoring Technology Dashboard for Azure
description: With the Azure Monitoring Technology Dashboard, you can monitor the health and performance of your Azure infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Understanding the Monitoring Technology Dashboard, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Monitoring Technology Dashboard for Azure

With the Azure Monitoring Technology Dashboard, you can monitor the health and performance of your Azure infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs.

## Monitoring Technology Dashboard for Azure overview

The Azure Monitoring Technology Dashboard shows the five CIs and servers with the highest metric readouts during the past six hours. The dashboard also shows the 50 most recent active alerts in your Azure environment. Based on the dashboard metrics, you might want to resize your CIs and servers to improve your system performance and efficiency.

To view the dashboard, navigate to **All** &gt; **AIOps Dashboards** &gt; **Monitoring Technology Dashboards** and select **Azure Monitoring**.

## Using the Monitoring Technology Dashboard for Azure

Before using the Monitoring Technology Dashboard for Azure:

-   Create an Azure credential. For details on creating Azure credentials, see [Create Azure cloud credentials](../../discovery/task/create-azure-cloud-credentials.md).
-   Create a Discovery schedule, using the credential created in the previous step. For details on creating a Discovery schedule, see [Azure Cloud Discovery](../../discovery/concept/azure-cloud-discovery.md).
-   Ensure that you’re working in the Agent Client Collector Monitoring scope in your ServiceNow instance.
-   Ensure that the agent\_client\_collector\_admin and dashboard\_admin roles are enabled.
-   Enable Metric Intelligence on the MID Server.
-   Ensure that the **Azure VM Metrics**, **Azure Storage Account Metrics**, **Azure Load Balancer Metrics**, **Azure Gateway Metrics**, and **Azure Redis Cache Metrics** policies are enabled
-   Ensure that the clotho plugin version 1.19.0.10 or above is enabled.

The Azure Monitoring Technology Dashboard contains the tabs that are listed in the following table.

|Tab|Description|
|---|-----------|
|Virtual Machines|Displays the metric data from the virtual machines in the Azure environment.|
|Storage Accounts|Displays the metric data from the storage accounts in the Azure environment.|
|Load Balancer|Displays the metric data from the load balancers in the Azure environment.|
|Application Gateway|Displays the metric data from the application gateway in the Azure environment.|
|Redis|Displays the metric data from the Redis cache in the Azure environment.|

Point to the relevant widget to view a specific datapoint and all of its details in a pop-up window.

You can filter the dashboard data according to the following filters:

|Filter name|Description|
|-----------|-----------|
|Time range filter|The time range for which you want metric data to display on the dashboard.|
|Metrics by selected CI filter|The CIs for which you want metric data to display on the dashboard.|

You can customize the appearance of the individual widgets on the Azure Monitoring Technology Dashboard. For example, you could change the time that the CPU usage on virtual machines is displayed. You can also include the customized widgets when you’re creating a custom dashboard. For more information, see [Customize the Monitoring Technology Dashboard](../task/customize-dashboard-widgets.md).

