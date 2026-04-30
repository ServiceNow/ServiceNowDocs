---
title: Import a schema from the Confluent Registry
description: Import a Schema from the Confluent Registry to enable your Stream Connect producers and consumers to send and receive Kafka messages in an Apache Avro format.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Schema management in Stream Connect, Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Import a schema from the Confluent Registry

Import a Schema from the Confluent Registry to enable your Stream Connect producers and consumers to send and receive Kafka messages in an Apache Avro format.

## Before you begin

-   Role required: kafka\_admin
-   This feature is part of schema management in Stream Connect. For more information, see [Schema management in Stream Connect](../concept/schema-management.md).
-   The ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin is required.
-   To import a schema, you need to have a Connection and Credential alias to connect to your Confluent registry. Navigate to **All** &gt; **IntegrationHub** &gt; **Schema Management** &gt; **Configure Connection** to configure your alias. For instructions, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## About this task

Stream Connect uses schemas to convert messages from plain text to an Avro format and back. Using an Avro format can reduce the size of the payload and simplify your integration to your local Kafka instance.

This document shows you how to import a schema from the Confluent registry. You can also [Create a standalone schema in Stream Connect](create-standalone-schema.md).

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Schema Management** &gt; **Import Schema from Confluent Registry**.

2.  Select the **Subject** of the schema you want to import from the Confluent Registry.

3.  Select the **Version** of the schema to import.

    The most recent version is the default.

4.  Select **Submit**.

    On the Confluent Stream Connect Schema form, the **Schema** field has the JSON-formatted schema that you imported from the registry, and the **Schema ID** field has the schema's ID.


## Result

Your schema is visible on the Stream Connect Schemas \[stream\_connect\_schema\] table and the Confluent Stream Connect Schema \[confluent\_stream\_connect\_schema\] table.

## What to do next

Use Stream Connect producers and consumers to send and receive messages in an Avro format.

**Parent Topic:**[Schema management in Stream Connect](../concept/schema-management.md)

