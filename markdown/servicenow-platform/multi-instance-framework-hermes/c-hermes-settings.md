---
title: Hermes Settings page
description: The Hermes Settings page is a centralized interface that enables Hermes administrators and maintenance users to monitor and control the configuration properties that govern the Hermes Messaging Service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/c-hermes-settings.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-05-21"
reading_time_minutes: 2
keywords: [Hermes, Hermes settings, Hermes configuration, hermes\_admin, maint, Kafka integration, system settings, background jobs]
breadcrumb: [Explore, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes Settings page

The Hermes Settings page is a centralized interface that enables Hermes administrators and maintenance users to monitor and control the configuration properties that govern the Hermes Messaging Service.

Access to the Hermes Settings page is role-based. The page displays the configurable properties to authorized users, along with descriptions, default values, and validation rules that help avoid misconfiguration. All configuration changes are traceable through built-in audit logging.

|Role|Access|
|----|------|
|maint|Has full visibility and edit access to all settings, including lower-level infrastructure properties.|
|hermes\_admin|Can view and modify a defined subset of properties relevant to topic management, Apache Kafka integration, and operational configuration.|

## Key benefits

-   View current and default values of all Hermes Messaging Service properties in one place.
-   Update values through a validated interface that enforces allowed ranges and formats.
-   Access descriptions that explain how each setting affects Hermes Messaging Service functionality.
-   Track changes to settings to support troubleshooting.

## Settings categories

The Hermes Messaging Service Settings page organizes properties into the categories listed in the following table.

|Category|Description|
|--------|-----------|
|Client Connection|Governs heartbeat polling intervals and timeout durations for cluster-side connectivity.|
|Health Status|Defines socket connection and read timeouts used by the Hermes Messaging Service Service Status monitor.|
|High Availability and Failover|Controls automatic failover behavior when health failures are detected.|
|IP Access Control|Enables or disables the IP ACL publishing mechanism and sets the publishing interval.|
|Kafka Integration|Controls topic manager timeouts, consumer and producer polling durations, retry limits, cache sizes, and metrics collection flags.|
|Logging and Health Metrics|Toggles debug logging and broker certificate expiration monitoring.|
|System Resources|Configures Hermes Messaging Service service cache limits and usage metrics batch query size.|
|Tokens|Manages token cache capacity, thread access limits, and idle eviction timing.|
|Topic Management|Controls topic cache size, cache idle time, thread limits, maximum partitions, and Topic Inspector display behavior.|

## Background jobs

Each settings category links to one or more background jobs that operate with the configurable properties. These jobs perform automated maintenance tasks such as heartbeat monitoring, metrics collection, metadata updates, cache cleanup, and IP ACL publishing. Jobs can be enabled, turned off, or have their intervals adjusted through the settings interface where applicable.

For a list of Hermes Messaging Service background jobs, see [Hermes background jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-settings-background-jobs.md).

## Implementation

The Hermes Messaging Service Settings page uses a Static Typed Wrapper approach \(`HermesGlideProperty`\) to define and expose settings. Each property holds its own validator, and validation rules are enforced at the point of change via `setOrThrow()`. This facilitates type safety at compile time, embedded validation, and reliable property management.

For information about viewing and modifying Hermes Messaging Service settings, see [Managing Hermes settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/manage-hermes-settings.md).

