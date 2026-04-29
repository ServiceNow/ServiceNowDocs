---
title: Monitoring Technology Dashboard for VMware vSphere
description: With the VMware vSphere Monitoring Technology Dashboard, you can monitor the health and performance of your VMware vSphere infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs and servers.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Understanding the Monitoring Technology Dashboard, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Monitoring Technology Dashboard for VMware vSphere

With the VMware vSphere Monitoring Technology Dashboard, you can monitor the health and performance of your VMware vSphere infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs and servers.

## Overview of the dashboard

The VMware vSphere Monitoring Technology Dashboard shows the five CIs and servers with the highest metric readouts during the past six hours. The dashboard also shows the 50 most recent active alerts in your VMware vSphere environment.

To view the dashboard, navigate to **All** &gt; **AIOps Dashboards** &gt; **Monitoring Technology Dashboards** and select **VMWare vSphere Monitoring**.

## Using the Monitoring Technology Dashboard for VMware vSphere

Before using the Monitoring Technology Dashboard for VMware vSphere:

-   Create a VMware vSphere credential and use it to create a Discovery schedule. For details on creating VMware vSphere credentials, see [Discovery for VMware](../../discovery/concept/vmware-cloud-discovery.md).
-   Create a Discovery schedule, using the credential created in the previous step. For details on creating a Discovery schedule, see [Discovery for VMware virtualization](../../discovery/concept/c_DiscoverVMwareInfrastructure.md).
-   Ensure that you’re working in the Agent Client Collector Monitoring scope in your ServiceNow instance.
-   Ensure that the agent\_client\_collector\_admin and dashboard\_admin roles are enabled.
-   Enable Metric Intelligence on the MID Server.
-   Ensure that the **VSphere Datacenter Metrics**, **VSphere Datastore Metrics**, **VSphere ESX Server Metrics** and **VSphere VirtualMachine Metrics** policies are enabled.

    Enabling these policies activates metric to CI mapping.

-   Ensure that the clotho plugin version 1.1.0 or above is enabled.
-   After upgrading from a previous version, follow the procedure described in the [ACC-M Dashboard Filters are not working when upgraded from Tokyo/Utah to Vancouver \[KB1438042\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1438042) article in the NOW Support Knowledge Base.

The VMware vSphere Monitoring Technology Dashboard contains the tabs listed in the following table.

|Tab|Description|
|---|-----------|
|VirtualMachine|Displays graphs of the top VMware vSphere VMs by metric type.|
|ESX Server|Displays graphs of the top VMware vSphere ESX servers by metric type.|
|Datacenter|Displays graphs of the top VMware vSphere datacenters by metric type.|
|Datastore|Displays graphs of the top VMware vSphere datastores by metric type.|
|Alerts|Displays the 50 most recent alerts that are associated with the URLs in your system. Alerts help you to remediate your system by providing information on problematic behavior.|

On the right side of widgets displaying a single metric, you can select the More options icon \(![More options icon](../image/three-vertical-icon.png)\) and select **Change group by**. Select the category you want to view the metric by: Host name, Class, Operating System, or OS Version.

Point to the relevant widget to view a specific datapoint and all of its details in a pop-up window.

You can filter the dashboard data according to the following filters:

| | |
|---|---|
|Time range filter|The time range for which you want metric data to display on the dashboard.|
|Metrics by selected CI filter|The CIs for which you want metric data to display on the dashboard.|

You can customize the appearance of the individual widgets on the VMware vSphere Monitoring Technology Dashboard. For example, you could change the timeframe for which the alerts appear. You can also include customized widgets when you are creating a custom dashboard. For more information, see [Customize the Monitoring Technology Dashboard](../task/customize-dashboard-widgets.md).

**Parent Topic:**[Understanding the Monitoring Technology Dashboard](monitor-tech-dashboard-concept.md)

