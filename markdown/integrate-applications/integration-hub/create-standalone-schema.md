---
title: Create a standalone schema in Stream Connect
description: Create a schema to enable your Stream Connect producers and consumers to send and receive Kafka messages in an Apache Avro format.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schema management, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Create a standalone schema in Stream Connect

Create a schema to enable your Stream Connect producers and consumers to send and receive Kafka messages in an Apache Avro format.

## Before you begin

-   Role required: kafka\_admin
-   This feature is part of schema management in Stream Connect. For more information, see [Schema management in Stream Connect](../concept/schema-management.md).
-   The ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin is required.

## About this task

Stream Connect uses schemas to convert messages from plain text to an Avro format and back. Using an Avro format can reduce the size of the payload and simplify your integration to your local Kafka instance.

This document shows you how to create your own standalone schema by uploading a JSON file or by entering a schema directly as a JSON-formatted string. You can also [Import a schema from the Confluent Registry](import-schema-confluent-registry.md).

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Schema Management** &gt; **Create Standalone Schema**.

    On the form to create an Avro schema, the value of the **Schema ID** is automatically filled in. You can keep the suggested value or change it.

    All schemas have a schema ID, a globally unique identifier of the schema. For standalone schemas, the schema ID is generated locally and is unique on the instance. By default, the generated schema ID value is the next highest available schema ID on the instance. For example, if your schemas have ID numbers one through five, the next schema you create will have a schema ID of six. Schema IDs are unique per registry. For example, two schemas can both have an ID of one as long as they're in different registries.

2.  In the **Source** field, select one of the following.

    |Option|Description|
    |------|-----------|
    |**File**|Select a JSON file to import the schema. Once imported, the contents of the file are visible in the **JSON schema** field.|
    |**Avro formatted String \(JSON\)**|Enter a schema in a JSON-string format.|

3.  Select **Submit**.

    On the Standalone Stream Connect Schema form, the **Schema** field has the JSON-formatted schema that you uploaded or entered.


## Result

Your schema is visible on the Standalone Stream Connect Schema \[standalone\_stream\_connect\_schema\] table and the Stream Connect Schemas \[stream\_connect\_schema\] table.

## What to do next

Use Stream Connect producers and consumers to send and receive messages in an Avro format.

**Parent Topic:**[Schema management in Stream Connect](../concept/schema-management.md)

