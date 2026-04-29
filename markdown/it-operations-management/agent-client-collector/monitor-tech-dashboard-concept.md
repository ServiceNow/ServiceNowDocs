---
title: Understanding the Monitoring Technology Dashboard
description: The Monitoring Technology Dashboard enables you to monitor server resources for the platform you select. The dashboard enables you to identify the CIs and servers in your system with the highest resource consumption, and the most recent active alerts.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Understanding the Monitoring Technology Dashboard

The Monitoring Technology Dashboard enables you to monitor server resources for the platform you select. The dashboard enables you to identify the CIs and servers in your system with the highest resource consumption, and the most recent active alerts.

You can customize the appearance of individual widgets on the Monitoring Technology Dashboard. For example, you could change the data parameters displayed for the CPU Utilization \(Linux\) metric, like the date range. You can include the customized widgets when creating a custom dashboard. For more information, see [Customize the Monitoring Technology Dashboard](../task/customize-dashboard-widgets.md).

The Monitoring Technology Dashboard shows the five CIs and servers with the highest metric readouts during the past six hours, and the 50 most recent active alerts on your OS's servers.

To enable viewing the Monitoring Technology Dashboard, ensure that you have installed clotho version 23.1.0.

To view the dashboard, navigate to **All** &gt; **AIOps Dashboards** &gt; **Monitoring Technology Dashboards** and select the OS whose metrics you want to view.

Select the arrow next to the dashboard name to enabled choosing a different dashboard to view:

![Arrow next to name of dashboard, with list of dashboards to choose](../image/monitoring-tech-db-linuxlabel.png)

-   **[Monitoring Technology Dashboard for Linux](monitor-tech-dashboard-linux.md)**  
With the Linux Monitoring Technology Dashboard, you can monitor the health and performance of your Linux infrastructure. The dashboard enables you to identify the CIs and servers in your system with the highest resource consumption, and also the most recent active alerts.
-   **[Monitoring Technology Dashboard for Windows](monitor-tech-dashboard-windows.md)**  
With the Windows Monitoring Technology Dashboard, you can monitor the health and performance of your Windows infrastructure. The dashboard enables you to identify the CIs and servers in your system with the highest resource consumption, and also the most recent active alerts.
-   **[Monitoring Technology Dashboard for HTTP](monitor-tech-dashboard-http.md)**  
With the HTTP Monitoring Technology Dashboard you can monitor the response time of your `http` and `https` URLs. By using the dashboard, you can identify the URLs with the highest metric readouts in your system's infrastructure, and view the most recent active alerts on those URLs.
-   **[Monitoring Technology Dashboard for Azure](monitor-tech-dashboard-azure.md)**  
With the Azure Monitoring Technology Dashboard, you can monitor the health and performance of your Azure infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs.
-   **[Monitoring Technology Dashboard for AWS](monitor-tech-dashboard-aws.md)**  
With the AWS Monitoring Technology Dashboard, you can monitor the health and performance of your AWS infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs and servers.
-   **[Monitoring Technology Dashboard for GCP](monitor-tech-dashboard-gcp.md)**  
With the GCP Monitoring Technology Dashboard, you can monitor the health and performance of your GCP infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs and servers.
-   **[Monitoring Technology Dashboard for VMware vSphere](monitor-tech-dashboard-vsphere.md)**  
With the VMware vSphere Monitoring Technology Dashboard, you can monitor the health and performance of your VMware vSphere infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs and servers.
-   **[Customize the Monitoring Technology Dashboard](../task/customize-dashboard-widgets.md)**  
Customize the Monitoring Technology Dashboard widgets in the Data Visualizations library so your dashboard displays information exactly as you want to see it.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](acc-endpoint-deployment.md)

