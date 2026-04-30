---
title: Metric Intelligence
description: ServiceNow Metric Intelligence provides the ability to capture, and then explore and analyze operational metrics data, identifying and indicating anomalies. Metric Intelligence generates anomaly alerts that can be promoted to IT alerts and appear on the Service Operations Workspace and service health dashboard. You can leverage this analysis to prevent potential service outages.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Metric Intelligence

ServiceNow® Metric Intelligence provides the ability to capture, and then explore and analyze operational metrics data, identifying and indicating anomalies. Metric Intelligence generates anomaly alerts that can be promoted to IT alerts and appear on the Service Operations Workspace and service health dashboard. You can leverage this analysis to prevent potential service outages.

-   **[Understanding Metric Intelligence](operational-intelligence-overview.md)**  
Use Metric Intelligence to identify and prevent potential service outages. Metric Intelligence, based on historical metric data, indicates anomalous behavior of CIs which events might not capture. Anomaly alerts can be promoted to regular IT alerts and appear on the Service Operations Workspace and service health dashboard for preventive actions.
-   **[MID Server and MID Server distributed cluster for Metric Intelligence](ops-intelligence-mid-server.md)**  
Using Metric Intelligence requires at least one MID Server distributed cluster which contains a single MID Server that is configured for Metric Intelligence.
-   **[Activating Metric Intelligence](../../agent-client-collector/concept/activating-metric-intelligence.md)**  
Metric Intelligence enables you to capture, explore and analyze operational metrics data, identifying and indicating anomalies. This analysis can prevent potential service outages.
-   **[Metric bounds sensitivity](../../agent-client-collector/concept/metric-bounds-sensitivity.md)**  
When measuring metrics in Insights Explorer, metric bounds may be overly sensitive, creating an abnormally large number of anomalies. When this happens, the system adjusts itself to ensure that fewer anomalies are created.
-   **[Metric binding](metric-binding.md)**  
After metric data is collected, Metric Intelligence identifies the CIs and the resources to bind the data to.
-   **[CIs in maintenance mode](cis-maintenance-mode.md)**  
Configure anomaly detection to exclude metrics for CIs that are in maintenance mode from model learning.
-   **[Metric Configuration Rules](../../agent-client-collector/concept/metric-configuration-rule.md)**  
Metric configuration rules enable you to determine how incoming metrics from the Agent Client Collector are to be processed.
-   **[Anomaly model testing](anomaly-model-test-concepts.md#)**  
Use anomaly model testing to apply and evaluate anomaly detection for a small set of CIs and metrics, using actual metric data. Compare test results to expected results, then fine-tune the anomaly detection model before enabling anomaly detection for the tested CIs and metrics in the production environment.
-   **[Advanced Promotion Engine](../../agent-client-collector/concept/advanced-promotion-engine.md)**  
You can create a definition for the Advanced Promotion Engine so that you can define the conditions for promoting the anomaly alerts to the All Alerts table. By promoting the alerts that meet the conditions, only the most relevant anomaly alerts move to the table.
-   **[Anomaly Alert Dashboard](anomaly-alert-dashboard.md)**  
View important anomaly alert reports in a single dashboard. Anomaly Alert Dashboard provides summaries about anomaly alerts and promoted alerts, in relation to Event Management alerts.
-   **[Metric Explorer](agent-workspace-ops-intelligence.md)**  
Metric Explorer provides an easy-to-navigate interface where service agents can view the health of a CI associated with an alert. Health details for a CI include various metric charts with control bounds, and aggregations for a time period.
-   **[Self-health monitoring for Metric Intelligence](self-health-monitoring-oi.md)**  
Use Event Management self-health monitors to monitor the health of Metric Intelligence infrastructure components and processes, and to alert about potential issues. Self-health monitoring allows you to proactively remediate issues and minimize data loss.
-   **[Domain separation and Metric Intelligence](domain-separation-operational-intelligence.md)**  
Domain separation is supported in Metric Intelligence. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Agent Client Collector Monitoring](../../agent-client-collector/concept/acc-monitoring-landing-page.md)

