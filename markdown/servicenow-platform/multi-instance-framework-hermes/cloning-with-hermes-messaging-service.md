---
title: Cloning with Hermes Messaging Service enabled
description: To clone your database from one instance to another successfully with Hermes enabled, you must ensure that certain Hermes tables are preserved and excluded. The list of tables in the preserve list should match those in the exclude list and vice versa.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Cloning with Hermes Messaging Service enabled

To clone your database from one instance to another successfully with Hermes enabled, you must ensure that certain Hermes tables are preserved and excluded. The list of tables in the preserve list should match those in the exclude list and vice versa.

Before you request a clone, verify the Hermes tables in the preserve and exclude lists. For example, make sure the sys\_kafka\_topic table is in the preserve list to maintain the current Hermes topics in the target instance. If the sys\_kafka\_topic table is not preserved, it is overwritten when the clone operation occurs.

The following sections assume that Hermes is installed on both the source and target instances before the clone. For example, if Hermes is not installed on the target instance, there are no Hermes tables to preserve.

**Important:** If you clone an instance without Hermes installed to an instance with Hermes installed, the Hermes tables in the target instance are removed.

To avoid losing this data, capture the data in the following Hermes tables using an update set:

-   hermes\_cluster\_config
-   hermes\_topics\_state
-   hermes\_topic\_location
-   hermes\_topics\_metrics
-   hermes\_metrics

You must ensure the hermes\_cluster\_config and hermes\_topic\_location tables are preserved to ensure the Hermes Messaging Service is functional.

## Hermes tables to preserve

Add the following Hermes tables to the Clone Data Preservers list if they're missing. Remove any Hermes tables that aren't in this list.

-   hermes\_app\_services
-   hermes\_audit\_operational\_metadata
-   hermes\_audit\_records
-   hermes\_client\_metrics
-   hermes\_cluster\_config
-   hermes\_metrics
-   hermes\_metrics\_collection
-   hermes\_system\_status
-   hermes\_topic\_audit\_records
-   hermes\_topic\_location
-   hermes\_topics\_metrics
-   hermes\_topics\_state
-   hermes\_usage\_metrics
-   sys\_kafka\_namespace
-   sys\_kafka\_topic

## Hermes tables to exclude

Add the following Hermes tables to the Clone Exclude Tables list if they're missing. Remove any Hermes tables that aren't in this list.

-   hermes\_app\_services
-   hermes\_audit\_operational\_metadata
-   hermes\_audit\_records
-   hermes\_client\_metrics
-   hermes\_cluster\_config
-   hermes\_metrics
-   hermes\_metrics\_collection
-   hermes\_system\_status
-   hermes\_topic\_audit\_records
-   hermes\_topic\_location
-   hermes\_topics\_metrics
-   hermes\_topics\_state
-   hermes\_usage\_metrics
-   sys\_kafka\_namespace
-   sys\_kafka\_topic

**Parent Topic:**[Administering Hermes Messaging Service](hermes-messaging-service-administration.md)

**Related topics**  


[Check the status of and connection to the Hermes Kafka cluster](../task/run-hermes-messaging-service-diagnostics.md)

[Monitoring data usage in Hermes](monitoring-data-usage-hermes.md)

[Tracking message usage in Hermes](tracking-hermes-messaging-service-usage.md)

[View Hermes Messaging Service log messages](../task/view-hermes-log-messages.md)

