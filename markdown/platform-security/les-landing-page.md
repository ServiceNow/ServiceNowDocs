---
title: Exploring Log Export Service \(LES\)
description: LES provides scalable, near real-time integration with analytic tools for security threat detection, performance optimization, and user experience monitoring. If you're new to LES, read this overview section to learn what the tool can do
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/les-landing-page.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Log Export Service \(LES\), Platform Security]
---

# Exploring Log Export Service \(LES\)

LES provides scalable, near real-time integration with analytic tools for security threat detection, performance optimization, and user experience monitoring. If you're new to LES, read this overview section to learn what the tool can do

Verify your entitlements to confirm you have access to Log Export Service.

## Log Export Service overview

LES enables you to use your analytic solutions to:

-   Detect ServiceNowsecurity threats and analyze security incidents
-   Troubleshoot and optimize ServiceNow application performance
-   Monitor and optimize ServiceNow user experience

LES leverages Hermes Messaging Service, a multi-tenant, multi-cluster data transport and queuing service built on Apache Kafka. This ServiceNow AI Platform capability enables your instance to produce and consume large volumes of Kafka events. Apache Kafka is an open-source data streaming platform that provides a single integration point for exchanging data across business systems.

\[Omitted image "les-architecture.png"\] Alt text: Diagram showing LES architecture with instance, Hermes Messaging Services, and analytic tools

LES forwards a copy of the log events as they are generated to Hermes Messaging Service. Hermes Messaging Service is available as part of Stream Connect, Log Export Service, and Instance Data Replication \(IDR\).

External log analytic systems, either in the cloud or on-premises, can consume the log events from Hermes Messaging Service. LES provides three connectivity options:

-   Dedicated MID Server: A dedicated MID Server installed on-premises or in the cloud automatically connects to Hermes Messaging Service, pulls log events continuously, and pushes them to log analytic tools through a REST connection.
-   Kafka connector from your log analytic solution: A Kafka connector from your log analytics product \(for example, Splunk\) installed on-premises or in the cloud automatically connects to Hermes Messaging Service, pulls log events continuously, and pushes them to log analytics tools.
-   Direct Kafka system connection: Your Kafka system connects directly with Hermes Messaging Service and uses native Kafka protocol commands to pull log events.

**Note:** If your Kafka message exceeds the configured memory buffer, Hermes returns an error indicating the message is larger than the configured total memory buffer.

To configure and manage LES, install it from ServiceNow Store. The LES application provides Guided Setups to install the service, pages to configure the service \(log sources, consumers, and destinations\), and reports to understand log creation and consumption.

**Note:** To create a custom source configuration, see [Create a log source configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-create-source-configuration.md).

## Log Export Service users

The following roles can use LES.

|Role|Description|
|----|-----------|
|Application admin \(sn\_logstoanalytics.admin\)|The LES application installs this role, allowing non-admin users to configure and manage LES.|
|System administrator \(admin\)|Required to install the LES Store application.|

## Log Export Service benefits

|Benefit|Feature|User|
|-------|-------|----|
|Create log source configuration to set filters on the logs|[Create a log source configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-create-source-configuration.md)|Application admin|
|Experience guided setup for Kafka consumers|[Guided setup for Kafka consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-guided-setup-kafka.md)|System administrator|
|Experience guided setup for MID server consumers|[Guided setup for MID Server consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-guided-setup-mid-server.md)|System administrator|
|Examine the log report dashboard to analyze the size of each data log|[Review log report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-use.md)|System administrator or Application admin|
|Replay historical log data from a supported table to backfill downstream systems retroactively|[Export existing logs on demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-export-existing-logs-on-demand.md)|Application admin or System administrator|

## What to explore next

To learn more about using Log Export Service, see:

-   [Administering Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-administer.md)
-   [Configuring Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-configure.md)
-   [Using Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-use.md)
-   [Log Export Service \(LES\) references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-references.md)

-   **[Log sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-log-sources-export.md)**  
Log Export Service \(LES\) can export log sources from some System Log Tables, Audit Tables, and Application Node Log Files.

**Parent Topic:**[Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-intro.md)

