---
title: Stream Producer
description: Stream Producer enables you to automatically stream changes from ServiceNow tables to Kafka topics using change data capture \(CDC\), eliminating the need for custom scripts or business rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/stream-producer.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 8
keywords: [Stream Producer, Change Data Capture, Kafka, Stream Connect, data export]
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Stream Producer

Stream Producer enables you to automatically stream changes from ServiceNow tables to Kafka topics using change data capture \(CDC\), eliminating the need for custom scripts or business rules.

Stream Producer provides a configuration-based alternative to writing scripts or business rules for exporting data. Instead of relying on error-prone manual solutions, you can define producers once and automatically stream table changes to external systems.

Stream Producer uses change data capture \(CDC\) technology to capture inserts, updates, and deletes on the tables you select. The captured changes are formatted as messages and sent to a Kafka topic, enabling real-time data synchronization with external applications.

## Key benefits

-   Eliminate dependency on business rules and custom scripts for data export.
-   Reduce performance impact on the ServiceNow instance.
-   Set it up once and automatically keep external data in sync.
-   Streamline complex data integration workflows.

## How it works

The following steps show the workflow for using Stream Producer.

1.  Create a Stream Producer configuration and specify a table to monitor.
2.  Define which change events to capture: insert, update, or delete.
3.  Select which fields to include in the payload \(or include all fields\).
4.  Configure an optional key and headers to accompany each message.
5.  Specify the target Kafka topic.
6.  Activate the producer.

Once activated, the Stream Producer automatically captures matching table changes and sends them to your Kafka topic without requiring any additional configuration or manual intervention.

## Supported features

-   Apply filters to capture only specific records.
-   Serialize payloads as plain text or in an Avro format.
-   Select individual fields or include all table fields.
-   Configure custom Kafka message keys with optional prefixes.
-   Add headers to messages with field values and metadata \(including action type and collection timestamp\).
-   Track producer statistics and activity metrics.
-   Manage multiple Stream Producers from a single console.

## Limitations

The following features aren't supported.

-   Large messages. If the message is larger than the max message size for the target Kafka environment, the message will fail to send and will be logged as `RecordTooLargeException`. The change record is skipped, and processing continues with the next change.
-   Message chunking for payloads over a size limit.
-   Interval-based change capture \(trigger only on scheduled intervals\).
-   File attachments.

## Change data capture operation

Stream Producer is built on a change data capture \(CDC\) framework, which provides a scalable, event-driven approach to detecting and exporting table changes. Rather than polling tables or relying on business rules, CDC captures changes at the database level and routes them through a message queue \(CDC queue\) for consumption by Stream Producer.

Stream Producer configurations define what data to capture, how to filter it, and where to send it. Once activated, the Stream Producer job runs continuously, processing change events and sending them to Kafka topics in your configured serialization format \(JSON or Avro\).

The following list provides an overview of how the CDC framework operates.

1.  Change detection: When a record is inserted, updated, or deleted in a monitored table, the CDC framework captures the change at the database level.
2.  CDC queue: The change is written to the Stream Connect CDC Change Queues \[`cdc_queue_stream_connect`\] table, with metadata including the table name, operation type \(insert/update/delete\), record sys\_id, and timestamp.
3.  Label assignment: Each Stream Producer configuration is assigned a label. Changes matching the producer's filter criteria are tagged with that label in the CDC queue.
4.  Producer polling: The Stream Producer job polls the CDC queue periodically, retrieving changes for its label.
5.  Payload construction: Stream Producer builds a message payload containing the specified fields and formats it according to your serialization choice.
6.  Kafka dispatch: The formatted message is sent to the configured Kafka topic.

## Key components

Stream Producer consists of the following components:

-   **Stream Producer configuration \(UI form\)**

    The user-facing interface where admins define producers. Contains sections for table information, filtering, and Kafka topic configuration. Managed by the Stream Producers \[`sys_sc_stream_producer`\] table. The **Active** field is read-only and automatically managed by the activation process.

-   **CDC Listener \(background service\)**

    Started when a Stream Producer is activated. Monitors the configured table for changes matching the filter criteria. Respects domain separation rules \(if applicable\).

-   **Stream Connect CDC Change Queues \[`cdc_queue_stream_connect`\]**

    Stores change events with labels identifying which Stream Producers should consume them. Index on labels field is not available; labeled lookups use full-table scans.

-   **Stream Producer Job**

    Scheduled batch job that polls the CDC queue, retrieves labeled changes, constructs payloads, and sends the payloads to Kafka. Runs every minute for a maximum of 2 minutes per execution. You can specify the maximum number of bytes written in a single Kafka transaction with the **glide.ih.kafka.stream\_producer.max\_kafka\_transaction\_bytes** property. The default value is 10MB.

-   **Stream Producer CDC Statistics \[`sys_sc_cdc_statistics`\]**

    Tracks metrics for each Stream Producer: messages and bytes produced, processing time, CDC depth \(queue depth\). Statistics are aggregated per job execution and updated periodically.

-   **Stream Producer \[`sys_sc_stream_producer`\]**

    Internal representation of an active producer. Created automatically when a Stream Producer is activated. Links the Stream Producer configuration to its runtime state and Kafka topic routing.


## Payload formats

Stream Producer supports two serialization formats for message payloads.

-   JSON \(human-readable, widely compatible\) and
-   Avro \(schema-versioned, compressed\).

You can select the serialization format when you [Create a Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/create-stream-producer.md). For more information about schema management for Avro, see [Schema management in Stream Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/schema-management.md).

## ISO format in JSON payloads

Date and time fields in JSON payloads are serialized to ISO 8601 formats.

-   Date fields are serialized to JSON as 2026-04-15.
-   All fields containing a date and time are serialized to JSON as 2026-04-15T00:29:38.000Z when stored in UTC, or as 2026-04-15T00:29:38.000 when stored in wall-clock time.
-   All fields containing only a time are serialized to JSON as 00:29:38Z when stored in UTC, or as 00:29:38 when stored in wall-clock time.
-   All Boolean, integer, and float fields are serialized as Boolean, integer, and float in JSON.
-   Payload fields that aren't dates, times, Booleans, or numbers aren't changed and continue to use `toString()`.

## Headers and metadata

Each message sent to Kafka includes optional headers that carry metadata about the change event. Headers enhance message routing and processing in downstream systems.

**Default headers:** When enabled, Stream Producer automatically adds the following headers to every message.

-   `action`: The type of change that triggered the message. Values are `insert`, `update`, or `delete`.
-   `collection_timestamp_ms`: The millisecond timestamp when the change was captured in the CDC queue.
-   `table_name`: The name of the source table being monitored.

**Custom headers:** You can configure additional headers using any fields from the source table. For reference or choice fields, headers include both the value and its display name, separated by a colon. For example, a reference field header might appear as `assigned_to: c39e3639876aba141444337e0ebb354f:Bob Person`.

## Domain separation support

Stream Producer follows domain separation rules. When domain separation is enabled:

-   Stream Producer configurations are scoped to a domain and can only see records visible to that domain.
-   The CDC Advisor \(change detection layer\) filters changes by domain, ensuring domain isolation.
-   Domain inheritance follows the ServiceNow domain hierarchy \(TOP → TOP/ACME, etc.\).
-   A Stream Producer in a parent domain can stream changes from child domains; a Stream Producer in a child domain can't access parent domain data.

## Security and permissions

Stream Producer implements multi-layer security controls to protect table access and sensitive data, including:

-   Role-based access control \(RBAC\) at the configuration and runtime layers.
-   Table deny-listing to restrict which tables can be monitored.
-   Automatic sensitive field filtering from payloads and schemas.

Role-based access control: Stream Producer configurations require specific roles to access and manage producers.

-   `kafka_producer`: Required to create, activate, and deactivate Stream Producer configurations.
-   `stream_connect_admin`: Administrative role with full access to Stream Producer management and Stream Producer \[`sys_sc_stream_producer`\] table operations.
-   `stream_connect_viewer`: View-only role. Users with this role can't access the Stream Producer configuration UI.

Table deny-listing: Only tables explicitly allowed by the platform or administrator configuration are selectable when defining Stream Producer configurations. This prevents users from inadvertently configuring producers on restricted or unsupported tables. Some table categories are typically allowed by default:

-   Incident, Problem, Change Request, and other ITSM tables.
-   Custom application tables \(with administrator approval\).
-   Integration-related tables that support external data synchronization.

**Note:** Accessing the deny-list requires the `maint` role \(only ServiceNow Support\).

Sensitive field filtering: Stream Producer automatically excludes sensitive field types from message payloads, Avro schemas, and UI displays to protect sensitive information, including:

-   `password`: User password fields.
-   `password2`: Secondary password fields or confirmation password fields.
-   `glide_encrypted`: Fields encrypted with the ServiceNow platform encryption mechanism.

## Plugin

Stream Producer requires the ServiceNow Stream Producer \[`com.glide.hub.stream_connect.stream_producer`\] plugin. This plugin is activated when you activate the ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin.

-   **[Create a Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/create-stream-producer.md)**  
Create a Stream Producer configuration to automatically stream table changes to a Kafka topic. You can specify which table to monitor, which change events to capture, which fields to include, and configure keys and headers for routing and tracking.
-   **[Activate or deactivate a Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/activate-stream-producer.md)**  
Activate a Stream Producer configuration to begin capturing and streaming table changes to your Kafka topic. You can deactivate it at any time to stop streaming changes. When you deactivate a producer, any unprocessed messages in the CDC queue are discarded.
-   **[Monitor and optimize Stream Producer performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/monitor-sc-performance.md)**  
Monitor Stream Producer performance metrics and change data capture \(CDC\) queue health to identify bottlenecks and optimize for your deployment scale and throughput requirements.

**Parent Topic:**[Using Stream Connect for Apache Kafka](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/stream-connect-apache-kafka.md)

