---
title: Plugins or applications installed with ITOM AIOps
description: Tables that list the plugins or applications that are installed with ITOM AIOps applications. When you update your application, any newly required application dependencies are installed.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Applying the CSDM guidelines to ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# Plugins or applications installed with ITOM AIOps

Tables that list the plugins or applications that are installed with ITOM AIOps applications. When you update your application, any newly required application dependencies are installed.

## Event Management

|Plugin or application name|Description|
|--------------------------|-----------|
|Alert Management Content \(com.em-alert-mgmt-content\)|Contains all the necessary base system subflows that can be used for alert remediation.|
|ITOM Licensing \(com.snc.itom.license\)|Central components for the ITOM Licensing Model, which calculates and displays how many subscriptions for ITOM applications your organization purchases and consumes.|
|Mid Web Server \(com.snc.sa.mid.webserver\)|A MID Server extension that enables developing REST APIs to send events and metrics to the MID Server. The plugin also enables the communication between the MID Server and Agent Client Collector.|
|Service Analytics \(com.snc.sa.analytics\)|Provides alert analytics based on machine learning \(ML\) and topology learning.|
|Event Management and Service Mapping Core \(com.snc.service-watch\)|Comprises the common components of Event Management and Service Mapping.|
|Tag Based Alert Clustering Engine \(sn\_em\_tbac\)|Provides a zero-code method that helps simplify alert grouping and performs alert correlation without the need for CMDB, model training, or fine-tuning.|
|Alert Rules Management \(sn\_em\_arm\)|Enables Event Management users to respond automatically to alerts. An alert management rule determines the required alert response.|

## Health Log Analytics

|Plugin or application name|Description|
|--------------------------|-----------|
|Integration Commons for CMDB \(sn\_cmdb\_int\_util\)|Contains a collection of utility functions that provide a common methodology for the processing of key CMDB attributes and is available to all CMDB certified integrations.|
|ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\)|Generates relevant topics for tenants, enabling them to transmit data from their customer infrastructure to ServiceNow automatically. These topics are predominantly intended for use with the Hermes Messaging Service.|
|Service Operations Workspace ITOM Apps \(sn\_sow\_itom\_cont\)|A configurable workspace that provides a unified experience for multiple IT Operations Management workflows. You can manage the life cycle of alerts in IT Operations Management workflows through simple, intuitive, and clear user interface, automated recommendations, and targeted experience.|
|Health Log Analytics Core \(com.glideapp.itom.occultus\)|Essential components for the Health Log Analytics scoped application.|
|Microsoft Teams Spoke for ServiceNow IntegrationHub \(com.sn.ms\_teams.ah\)|Provides actions that a process analyst can use when designing flows to automate sending messages about ServiceNow incident and problem records to a Microsoft Teams channel.|
|Slack Webhooks Spoke for ServiceNow IntegrationHub \(com.sn.slack.ah\)|Use Slack webhooks to post messages and record details for ServiceNow incidents, problems, and changes to Slack channels.|
|Normalization Data Services Client \(com.glide.data\_services\_canonicalization.client\)|Helps maintain consistency by checking that records for a given company match the list of standard company names. If the plugin finds a company-name field with a variant of that name, it substitutes the standard name in its place.|

## Service Reliability Management

|Plugin or application name|Description|
|--------------------------|-----------|
|Service Operations Workspace Service Reliability Management \(SRM\) Common \(sn\_sow\_srm\_common\)|Delivers common utilities and configuration settings used by Service Reliability Management such as core functionality related to managing teams and services, and metric calculation for services.|
|Service Reliability Management \(Global dependencies\) \(com.snc.srm\)|Supports global scripts and utilities for Service Reliability Management for Service Operations Workspace.|
|Event Management \(com.glideapp.itom.snac\)|Helps you to identify health issues across business services and infrastructure on a single management console. Event Management provides intelligent event and alert processing, including automatic alert remediation, aggregation, and root cause analysis \(RCA\)|
|Service Operations Workspace ITOM Apps \(sn\_sow\_itom\_cont\)|A configurable workspace that provides a unified experience for multiple IT Operations Management workflows. You can manage the life cycle of alerts in IT Operations Management workflows through simple, intuitive, and clear user interface, automated recommendations, and targeted experience.|
|On-Call Scheduling \(com.snc.on\_call\_rotation\)|Provides the ability to create on-call schedules and escalation trees. When an incident is created, you can dynamically route the escalation to an on-call resource.|
|SOW - Alert Automation \(sn\_sow\_alert\_rules\)|Provides operators in Service Operations Workspace with the ability to create and manage alert automation for their team. This automation can be used to enrich, process, and group alerts.|
|Service Level Objective Management for Service Operations Workspace \(sn\_sow\_slo\)|Includes features to monitor and manage service health using Service Level Indicators \(SLIs\), Service Level Objectives \(SLOs\), and error budgets.|

## Service Operations Workspace for ITOM

|Plugin or application name|Description|
|--------------------------|-----------|
|Service Operations Workspace Core \(sn\_sow\)|Core capabilities and workspace configurations for Service Operations Workspace.|
|Event Management Core \(sn\_em\_ai\)|Enables you to track and monitor alerts in the ServiceNow Agent Workspace.|
|Service Operations Workspace Integrations launchpad \(sn\_itom\_integ\_app\)|Provides a new and enhanced experience for viewing, configuring, and managing all your available ITOM AIOps integrations.|
|Service Operations Workspace Alert Mngmt \(sn\_sow\_em\)|A detailed alert record page with supplementary data such as Quick Overview, Playbook, and Metrics tabs.|
|Service Operations Workspace Express List \(sn\_itom\_aiops\_list\)|A centralized and consolidated platform that enables operators to triage, analyze, and remediate alerts, all in one place. Express List provides a live view of alerts, dynamic filtering, a preview panel with additional context and essential details about each alert, and automated technical analysis using Now Assist.|
|Service Operations Workspace Log Analytics \(sn\_sow\_hla\)|A log viewer in Service Operations Workspace. The application also includes the custom Elasticsearch data source for Performance Analytics \(PA\) dashboards.|
|AIOps Dashboards \(sn\_aiops\_dashboard\)|Offers comprehensive visualizations of critical operational data and actionable insights that facilitate proactive responses to potential issues. The application targets multiple ITOM personas with different needs, enabling you to monitor key performance indicators \(KPIs\), track service health, and gain valuable context on the overall IT environment.|
|Event Management Connectors \(sn\_em\_connector\)|A collection of predefined interfaces \(connectors\) for ingesting events from third-party monitoring tools or Agent Client Collector into a ServiceNow instance.|
|Service Operations Workspace UI Components \(sn\_itom\_uib\_comp\)|A joined repository for holding common internal UI components.|

## Metric Intelligence

|Plugin name|Description|
|-----------|-----------|
|Operational Intelligence - Extension Health Monitoring \(com.snc.sa.metric.health\)|Contains some features that enable self-monitoring capabilities for the Metric Intelligence components in the MID Server.|
|Highcharts Reporting \(com.glide.highcharts\)|Provides some UI functionality to Metric Intelligence.|
|Event Management \(com.glideapp.itom.snac\)|Helps you to identify health issues across business services and infrastructure on a single management console. Event Management provides intelligent event and alert processing, including automatic alert remediation, aggregation, and root cause analysis \(RCA\)|
|ITOM UI Components \(com.snc.itom.ui\)|Shared UI components for ITOM products that provide some UI functionality to Metric Intelligence.|
|MID Server Distributed Cluster \(com.snc.agent.distributed.cluster\)|Enables management of the mid cache component of Metric Intelligence from the ServiceNow instance.|
|List v3 Components \(com.glide.ui.list\_v3\_components\)|Provides some UI functionality to Metric Intelligence and components required for List v3, including REST endpoints, directives, and templates.|
|MetricBase \(com.snc.clotho\)|The database where the raw metric data such as CPU usage and Disk Free is saved and where model fitting for anomaly detection occurs.|
|Mid Web Server \(com.snc.sa.mid.webserver\)|A MID Server extension that enables developing REST APIs to send events and metrics to the MID Server. The plugin also enables the communication between the MID Server and Agent Client Collector.|

## Agent Client Collector

|Plugin or application name|Description|
|--------------------------|-----------|
|Agent Client Collector Global Utilities \(com.snc.sa.accutils\)|A set of globally scoped utilities that facilitates cross-scope transactions between Agent Client Collector Framework and a ServiceNow instance.|
|Configuration Management For Scoped Apps \(CMDB\) \(com.snc.cmdb.scoped\)|Provides scoped applications with access to Identification Engine APIs.|
|Mid Web Server \(com.snc.sa.mid.webserver\)|A MID Server extension that enables developing REST APIs to send events and metrics to the MID Server. The plugin also enables the communication between the MID Server and Agent Client Collector.|

|Plugin or application name|Description|
|--------------------------|-----------|
|Agent Client Collector Framework \(sn\_agent\)|Manages Agent Client Collector on the ServiceNow instance and the MID Server.|
|Metric Intelligence \(sn\_metrics\_ng\)|A companion application to the family Metric Intelligence plugin that provides additional functionality and enhancements.|
|Service Operations Workspace Metric Explorer \(sn\_itom\_metric\_exp\)|Enables operators to investigate metric behavior and compare and correlate different metrics across hosts, applications, and services so they can troubleshoot issues and find the root cause.|
|Event Management \(com.glideapp.itom.snac\)|Helps you to identify health issues across business services and infrastructure on a single management console. Event Management provides intelligent event and alert processing, including automatic alert remediation, aggregation, and root cause analysis \(RCA\)|
|Metric Intelligence \(com.snc.sa.metric\)|Provides the ability to capture, explore and analyze application metrics data, identifying and indicating anomalies. Metric Intelligence generates anomaly alerts, which can be promoted to IT alerts and appear on the Service Operations Workspace and Service Health dashboard.|

|Plugin or application name|Description|
|--------------------------|-----------|
|Agent Client Collector for Visibility - Content Content \(sn\_acc\_vis\_content\)|Provides agent-based infrastructure discovery and collects Software Asset Management \(SAM\) metrics to support Discovery and Digital End-User Experience \(DEX\) applications.|
|Discovery \(com.snc.discovery\)|Finds applications and devices on your network, and then updates the CMDB with the information it finds.|
|Agent Client Collector Framework \(sn\_agent\)|Manages Agent Client Collector on the ServiceNow instance and the MID Server.|
|CMDB CI Class Models \(sn\_cmdb\_ci\_class\)|Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. Applications such as Discovery and Service Mapping can use these class extensions to populate configuration items \(CIs\) and discover various technologies and software.|

|Application name|Description|
|----------------|-----------|
|Agent Client Collector Monitoring \(sn\_itmon\)|Provides the ability to monitor your configuration items \(CIs\). This application comes with predefined monitoring checks and policies that are applied on the agent.|
|Health Log Analytics \(sn\_occ\)|Helps you solve issues faster by ingesting, analyzing, and correlating machine-generated log data in real-time to predict IT issues before they affect you.|

|Plugin or application name|Description|
|--------------------------|-----------|
|Security Incident Response \(sn\_si\)|Enables you to manage and automate the life cycle of your security incidents from initial prioritization to containment and resolution. Use the automated workflows to respond quickly and consistently, and understand trends and bottlenecks through the data provided by analytics-driven dashboards and comprehensive reporting systems.|
|Security Support Orchestration \(sn\_sec\_cmn\_orch\)|Dependency for the Vulnerability Response and Security Incident Response applications.|
|Threat Intelligence Support Common \(sn\_ti\)|Enables you to find Indicators of Compromise \(IoCs\) and enrich security incidents with threat intelligence data. Threat Intelligence enables you to access and provide a reference point for your company's Structured Threat Information Expression \(STIX\) data.|
|Agent Client Collector Spoke \(sn\_acc\_spoke\)|Provides a framework to write customized workflows or automations to execute on agents or CIs.|
|Security Support Core \(com.snc.security\_support.core\)|Provides a robust core data model and UI framework specifically for security operations integrations. This comprehensive model serves as the backbone for seamlessly integrating various security tools and systems, promoting smooth data flow and efficient operations.|
|Security Support Common \(sn\_sec\_cmn\)|Enables core functionality used by the Security Operations applications.|
|Security Integration Framework \(sn\_sec\_int\)|Manages the common functionality for Security Operations integrations including both Security Incident Response and Vulnerability Response. Security Integration Framework enables you to use existing features and functionality without having to reimplement them.|
|Agent Client Collector Framework \(sn\_agent\)|Manages Agent Client Collector on the ServiceNow instance and the MID Server.|
|Vulnerability Response Dependencies \(com.snc.si\_dep\)|Activates all the dependent plugins required to support the Vulnerability Response application.|

## Service Observability

|Plugin or application name|Description|
|--------------------------|-----------|
|Service Observability UI \(sn\_service\_obs\_ui\)|Enables you to use Service Observability in the Service Operations Workspace \(SOW\) and the SOW Admin Center.|
|Service Reliability Management \(sn\_sow\_srm\)|Service Reliability Management and Service Observability display service performance metrics together to give a holistic view into service health.|
|Platform Analytics \(sn\_app\_analytics\_w\)|Enables customizing the dashboards.|

**Related topics**  


[Plugins or applications installed with ITOM Cloud Accelerate](../../itom-cloud-accelerate/reference/plugin-app-cloud-accelerate.md)

[Plugins or applications installed with ITOM Visibility](plugin-app-itom-visibility.md)

[Plugins activated with ITOM Optimization](plugin-itom-optimization.md)

[Applications installed with Now Assist for ITOM](../../now-assist-itom/reference/app-now-assist-itom.md)

