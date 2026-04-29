---
title: Deploying Agent Client Collector on endpoints
description: When deploying the Agent Client Collector, perform deployment and management tasks on your endpoints.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Deploying Agent Client Collector on endpoints

When deploying the Agent Client Collector, perform deployment and management tasks on your endpoints.

Endpoint deployment connects agents directly to the ServiceNow® cloud through ITOM Cloud Services \(ICS\). Agents on laptops, remote offices, and distributed sites reach ICS over the internet using a secure connection, without a MID Server. ServiceNow® manages the infrastructure and issues certificates automatically.

Choose endpoint deployment when your agents operate beyond the data center, where maintaining MID Servers isn't practical. Digital End-User Experience \(DEX\) requires this architecture, and Agent Client Collector for Visibility - Content \(ACC-VC\) supports it in specific use cases.

-   **[Configuring MID-less Agent Client Collector](acc-configuring-without-mid.md)**  
Configure MID-less Agent Client Collector to enable sending information through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
-   **[Configure an agent registration key](../task/agent-registration-key-configuration.md)**  
Configure an agent registration key so that you can deploy MID-less Agent Client Collector. Deploying MID-less Agent Client Collector enables you to use the MID Server for more persistent resources.
-   **[Agent Client Collector installation on a macOS system](acc-install-mac-os.md)**  
Install Agent Client Collector on a system that uses macOS. You can either use a single-line command script or follow a manual installation procedure if the agent is not connected to the instance or you want enhanced customization options.
-   **[Perform Zscaler remediation](zscaler-remediation-concept.md)**  
If the Zscaler application installed on your Windows or macOS agent is not running efficiently, you can stop and start the app. This process is called **remediation**. Running remediation automatically creates an incident on the agent. You can also view Zscaler statuses on the Zscaler dashboard as a graph.
-   **[Choose and configure metrics to monitor](../../event-management/task/configure-metric-monitors.md)**  
Metric Intelligence uses data sources that can be monitoring hundreds of metrics for all CIs. Choose for each data source type which details are important for which CIs, and then activate or deactivate the respective monitor type to control the amount of data that is being processed.
-   **[Create a configuration settings rule](../../event-management/task/create-config-overriding-rule.md)**  
Configuration settings affect how metric data is processed. Configuration settings rules override the default metric processing behavior to determine the system actions when an anomaly is detected.
-   **[Understanding the Monitoring Technology Dashboard](monitor-tech-dashboard-concept.md)**  
The Monitoring Technology Dashboard enables you to monitor server resources for the platform you select. The dashboard enables you to identify the CIs and servers in your system with the highest resource consumption, and the most recent active alerts.
-   **[Setting exclusion lists for IPs and NICs](acc-v-set-exclusion-lists-for-ips-and-nics.md)**  
Agent Client Collector for Visibility - Content \(ACC-VC\) version 1.3.0 supports exclusion list for IPs and Network Interface Controllers \(NICs\) with a flexible mechanism for filtering out values for IPs and or NICs when creating or updating the host CI and related items.
-   **[Identify software editions on Windows devices](../task/identify-sw-edition.md)**  
Determine which edition of software is in use on Windows devices in your environment, to maintain an accurate software inventory. Software products commonly support multiple editions, making it difficult to identify which edition is in use.
-   **[Generate a Pattern allow list](../task/generate-patterns-allow-list.md)**  
Generate an allow list for a specific scope or selection of patterns.

**Parent Topic:**[Agent Client Collector](acc-landing-page.md)

