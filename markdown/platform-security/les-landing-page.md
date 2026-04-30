---
title: Log Export Service \(LES\)
description: Log Export Service \(LES\) lets you seamlessly export your instance system and application logs into your enterprise security analytic tools. The service provides a highly scalable and near real-time integration with your analytic tools that is easy to setup and maintain.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Platform Security]
---

# Log Export Service \(LES\)

Log Export Service \(LES\) lets you seamlessly export your instance system and application logs into your enterprise security analytic tools. The service provides a highly scalable and near real-time integration with your analytic tools that is easy to setup and maintain.

The integration tool allows you to leverage your analytic solutions to perform the following:

-   Detect ServiceNow security threats and analyze security incidents
-   Troubleshoot and optimize ServiceNow app performance
-   Monitor and optimize ServiceNow user experience

LES leverages a ServiceNow AI Platform capability called the Hermes Messaging Service, which is a multi-tenant, multi-cluster, data transport, and queuing service built on Apache Kafka that enables your instance to produce and consume large volumes of Kafka events. Apache Kafka is an open-source data streaming platform that provides a single integration point for exchanging data across business systems in your organization.

![](../image/les-architecture.png)

LES forwards a copy of the log events as they are generated to the Hermes Messaging Service.

The Hermes Messaging Service is a multi-tenant, multi-cluster, data transport, and queuing service built on Apache Kafka that enables your instance to produce and consume large volumes of Kafka events. The Hermes Messaging Service is a ServiceNow AI Platform capability that is available as part of Stream Connect, Log Export Service \(LES\), and Instance Data Replication \(IDR\).

The external log analytic systems, either in the cloud or on-prem, can use and consume the log events from the Hermes Messaging Service. LES provides three connectivity options to consume the logs:

-   Dedicated MID Server: A dedicated MID Server is installed on-prem or in the cloud that automatically connects to Hermes Messaging Service, pulls log events from it continuously and then pushes them to log analytic tools via a REST connection.
-   Leverage Kafka connector from your log analytic solution \(for example, Splunk\): A Kafka connector from your log analytics product of choice is installed on-prem or in the cloud that automatically connects to Hermes Messaging Service, pulls log events from it continuously and then pushes them to log analytics tools.
-   Directly from your Kafka system: Your Kafka system connect directly with the Hermes Messaging Service and use its native Kafka protocol commands and connectivity to pull logs events from it.

To configure and manage LES you need to install the it from ServiceNow Store. The LES application provides Guided Setups to help you install the service, pages to configure the service \(log sources, consumers and destinations\) and reports to understand log creation and consumption.

![](../image/les-module.png)

**Note:** You can also create a new source configuration. See [Create a log source configuration](../task/les-create-source-configuration.md) for more information.

-   **[Log Export Service roles](../reference/les-roles.md)**  
Log Export Service is installed with these roles.
-   **[Log sources](les-log-sources-export.md)**  
Log Export Service \(LES\) can export log sources from some System Log Tables, the Audit Table, and Application Node Log Files.
-   **[Create a log source configuration](../task/les-create-source-configuration.md)**  
Regulate and set filters on the logs to be forwarded by creating a log source configuration.
-   **[Kafka consumer](les-kafka-consumer.md#)**  
Use guided setup to step through the initial configuration of LES. Guided setup assists you with planning the roll-out of the product and performing the basic configuration to go live.
-   **[MID server consumer](les-mid-server-consumer.md#)**  
Use guided setup to step through the initial configuration of LES. Guided setup assists you with planning the roll-out of the product and performing the basic configuration to go live.
-   **[Set up a secure connection to the Hermes Messaging Service for LES](../task/les-hermes-cert.md)**  
Secure your Kafka topics by generating a ServiceNow® instance-signed certificate.
-   **[Review log report](../task/les-review-log-exports.md)**  
Analyze the size of each data log by reviewing the log report dashboard.

**Parent Topic:**[Platform Security](../../general/concept/platsec-sublanding.md)

