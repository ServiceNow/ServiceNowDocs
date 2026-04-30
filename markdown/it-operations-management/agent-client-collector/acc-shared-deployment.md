---
title: Agent Client Collector deployment - shared between servers and endpoints
description: When deploying the Agent Client Collector, there are components which are shared between servers and endpoints.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-02-01"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Agent Client Collector deployment - shared between servers and endpoints

When deploying the Agent Client Collector, there are components which are shared between servers and endpoints.

-   **[Checks and policies](checks-policies.md)**  
A check is a combination of a command and its configuration. The check is executed on the Agent Client Collector's devices to gather data from those devices.
-   **[Agent Client Collector configuration data files](acc-config-data-files.md)**  
Configuration data files store dynamic instance data, such as virtual machine details, that check definitions use during execution. This ensures that checks are executed with up-to-date and accurate information about the instance being monitored.
-   **[Agent Client Collector API](acc-api.md)**  
Use the Agent Client Collector \(ACC\) API to create a flow that executes an `osquery` command on agents and processes the results. By leveraging the ACC API, you can automate the querying of agent data and streamline the processing of results, making it easier to monitor and manage system performance.
-   **[Agent Client Collector health instance scan suite](acc-instance-scan-suite.md)**  
The Agent Client Collector \(ACC\) health instance scan suite consists of checks that detect anomalies and other issues that might occur on your instance. These checks are designed to ensure the overall health and performance of the ACC, proactively identifying potential problems before they impact system operations.
-   **[Agent Client Collector certificates](acc-certificates.md)**  
Agent Client Collector certificates verify the authenticity of your agents, servers, and users. Using Agent Client Collector certificates ensures the safety of your environment.
-   **[Using Agent Client Collector logs](logs-acc.md)**  
Use Agent Client Collector logs to track events in your system. Log levels indicate the severity of each event.
-   **[Configure the Google Cloud Platform \(GCP\) configuration data file](../task/gcp-config-data-file.md)**  
Configure the Google Cloud Platform \(GCP\) configuration data file to monitor metrics in your GCP environment.
-   **[Configure the action level for anomaly detection](../../event-management/concept/configure-level-anomaly-detection.md)**  
Create a configuration setting rule that refines the level of anomaly detection processing and analysis that is applied to specific CIs and metrics. Set a processing level that reflects the importance of metrics at different stages of implementation, to reduce data load if needed.
-   **[Create Azure policies for metric collection](../task/create-policies-azure.md)**  
Create your own policies to enable Azure to collect the metrics for the resources that have policies that don’t come with the base system. The Azure Metrics Collector check brings the metrics to the agent through the Azure Metrics Batch API.
-   **[Block event creation for non-existent entities](../task/prevent-events-nonexistent-entities.md)**  
Invoke the **skip\_events\_for\_nonexistent** parameter to block event creation when specific process, service, or log does not exist. Invoke this parameter if you do not want to be notified about these non-existent entities.
-   **[Enable viewing HAProxy metrics](../task/configure-haproxy-metrics-stats-page.md)**  
Configure the HAProxy metrics stats page to enable monitoring your system devices by viewing HAProxy metrics.
-   **[Enable Apache Kafka health monitoring](../task/enable-kafka-metrics.md)**  
Set configurations in the Apache HTTP server application to enable the Agent Client Collector to perform Apache Kafka HTTP server monitoring.
-   **[Enable running of Varnish checks](../task/discover-varnish-ci.md)**  
Use application fingerprints to discover the Varnish CI, to enable running Varnish checks.
-   **[Detecting portable applications using push-based discovery](acc-v-detect-portable-apps.md)**  
Portable applications are those applications that don’t need to be installed on the target system. Starting in ACC-VC version 2.3.0, push-based Discovery can detect portable applications, such as Firefox, VLC, Notepad++ etc, for Windows only.
-   **[Cloud Native Operations for Visibility](../../cloud-native-operations-visibility/concept/cnov-landing.md)**  
Cloud Native Operations for Visibility \(CNO for Visibility\) has been renamed Agent Client Collector for Kubernetes – Visibility. The term Cloud Native Operations for Visibility has been deprecated.
-   **[Enabling Agent Client Collector data collection](data-collection-enabling.md)**  
You can perform actions which enhance data collection from the hosts on which Agent Client Collector is running.

**Parent Topic:**[Agent Client Collector](acc-landing-page.md)

