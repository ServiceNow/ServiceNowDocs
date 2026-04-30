---
title: Exploring Log Export Service \(LES\)
description: The LES service provides a highly scalable and near real-time integration with your analytic tools that is easy to set up and maintain. If you're new to LES, read this overview section to learn what the tool can do.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Log Export Service \(LES\), Platform Security]
---

# Exploring Log Export Service \(LES\)

The LES service provides a highly scalable and near real-time integration with your analytic tools that is easy to set up and maintain. If you're new to LES, read this overview section to learn what the tool can do.

Check your entitlements to determine whether you have access to Log Export Service.

## Log Export Service overview

The integration tool allows you to leverage your analytic solutions to perform the following:

-   Detect ServiceNow security threats and analyze security incidents
-   Troubleshoot and optimize ServiceNow app performance
-   Monitor and optimize ServiceNow user experience

LES leverages a ServiceNow AI Platform capability called the Hermes Messaging Service, which is a multi-tenant, multi-cluster, data transport, and queuing service built on Apache Kafka that enables your instance to produce and consume large volumes of Kafka events. Apache Kafka is an open-source data streaming platform that provides a single integration point for exchanging data across business systems in your organization.

![Log Export Service](../image/les-architecture.png)

LES forwards a copy of the log events as they're generated to the Hermes Messaging Service.

The Hermes Messaging Service is a multi-tenant, multi-cluster, data transport, and queuing service built on Apache Kafka that enables your instance to produce and consume large volumes of Kafka events. The Hermes Messaging Service is a ServiceNow AI Platform capability that is available as part of Stream Connect, Log Export Service \(LES\), and Instance Data Replication \(IDR\).

The external log analytic systems, either in the cloud or on-prem, can use and consume the log events from the Hermes Messaging Service. LES provides three connectivity options to consume the logs:

-   Dedicated MID Server: A dedicated MID Server is installed on-prem or in the cloud that automatically connects to Hermes Messaging Service, pulls log events from it continuously and then pushes them to log analytic tools via a REST connection.
-   Leverage Kafka connector from your log analytic solution \(for example, Splunk\): A Kafka connector from your log analytics product of choice is installed on-prem or in the cloud that automatically connects to Hermes Messaging Service, pulls log events from it continuously and then pushes them to log analytics tools.
-   Directly from your Kafka system: Your Kafka system connect directly with the Hermes Messaging Service and use its native Kafka protocol commands and connectivity to pull logs events from it.

**Note:** If your Kafka message exceeds the configured memory buffer, Hermes may return an error indicating that it's larger than the total memory buffer you've configured.

To configure and manage LES you need to install it from ServiceNow Store. The LES application provides Guided Setups to help you install the service, pages to configure the service \(log sources, consumers and destinations\) and reports to understand log creation and consumption.

![Navigation filter](../image/les-module.png)

**Note:** You can also create a new source configuration. See [Create a log source configuration](../task/les-create-source-configuration.md) for more information.

## Log Export Service users

Log Export Service has the following users.

|Users|Description|
|-----|-----------|
|Application admin \[sn\_logstoanalytics.admin\]|This role is installed along with the LES application and allows a non-admin to use the application.|
|System administrator \[admin\]|Admin role is required for the setup of the LES store application.|

## Log Export Service benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Create log source configuration to set filters on the logs|[Create a log source configuration](../task/les-create-source-configuration.md)|Application admin|
|Experience guided setup for Kafka consumers|[Guided setup for Kafka consumers](../task/les-guided-setup-kafka.md)|System administrator|
|Experience guided setup for MID server consumers|[Guided setup for MID Server consumers](../task/les-guided-setup-mid-server.md)|System administrator|
|Examine the log report dashboard to analyze the size of each data log|[Review log report](les-use.md#)|System administrator or Application admin|

## What to explore next

To learn more about using Log Export Service, see:

-   [Administering Log Export Service \(LES\)](les-administer.md)
-   [Configuring Log Export Service \(LES\)](les-configure.md)
-   [Using Log Export Service \(LES\)](les-use.md#)
-   [Log Export Service \(LES\) references](les-references.md)

-   **[Log sources](les-log-sources-export.md)**  
Log Export Service \(LES\) can export log sources from some System Log Tables, the Audit Table, and Application Node Log Files.

**Parent Topic:**[Log Export Service \(LES\)](les-intro.md)

