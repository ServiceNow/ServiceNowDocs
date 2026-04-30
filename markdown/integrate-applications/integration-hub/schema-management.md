---
title: Schema management in Stream Connect
description: Import and create schemas to send and receive messages in an Apache Avro format. Using an Avro format can reduce the size of the payload and simplify your integration to your local Kafka instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Data and Automation]
---

# Schema management in Stream Connect

Import and create schemas to send and receive messages in an Apache Avro format. Using an Avro format can reduce the size of the payload and simplify your integration to your local Kafka instance.

Avro is an open-source data-serialization system that uses schemas to structure encoded data. With an Avro schema, data can be converted from plain-text JSON to an Avro binary format and back. You can store schemas in ServiceNow, so your Stream Connect producers and consumers can use the schemas to serialize Avro messages.

The following image shows an overview of schema management in Stream Connect. Schemas, stored in schema registries, enable messages in producers and consumers to be converted from plain text to an Avro format and back.

![Diagram showing how Stream Connect uses schemas stored in the schema registries to convert Kafka messages into different formats.](../images/stream-connect-schema-diagram.png)

## Schemas

You can import a schema from the Confluent registry or create your own standalone schema by uploading a JSON file or entering a schema directly as a JSON-formatted string.

After your schema is imported or created, you can see it on the Stream Connect Schemas \[stream\_connect\_schema\] table, which stores both Confluent and standalone schemas. Additionally, Confluent schemas are visible on the Confluent Stream Connect Schema \[confluent\_stream\_connect\_schema\] table. Standalone schemas are on the Standalone Stream Connect Schema \[standalone\_stream\_connect\_schema\] table.

All schemas have a schema ID, a globally unique identifier of the schema. For Confluent schemas, the schema ID is imported from the Confluent registry. For standalone schemas, the schema ID is generated locally and is unique on the instance. By default, the generated schema ID value is the next highest available schema ID on the instance. For example, if your schemas have ID numbers one through five, the next schema you create will have a schema ID of six. You can change the default value.

Schema IDs are unique per registry. For example, two schemas can both have an ID of one as long as they're in different registries.

## Schema registries

Every schema belongs to a registry. There are two types of schema registries in ServiceNow: the Confluent Schema Registry and the Standalone Schema Registry.

Both schema registries have an option to **Track in the update set**. When this option is enabled, the schemas in that registry are saved to the update set. Saving the schemas to the update set makes it possible to move them from one environment to another. By default, this option is turned off for the Confluent Schema Registry because schema IDs may change from one environment to another. This option is enabled for the Standalone Schema Registry, because if you're creating schemas manually, the schema ID is less likely to change from one environment to another. To change the default setting for either registry, navigate to **All** &gt; **IntegrationHub** &gt; **Schema Registries**, select the registry, and change the **Track in the update set** option.

## Wire-level message format

For interoperability, ServiceNow uses a wire-level message format similar to the ones used by other systems. The first byte is set to 0. The next 4 bytes are used for the schema ID. The remaining bytes are used for the data, serialized in an Avro format.

<table id="table_rhd_vjy_jbc"><tbody><tr><td>

Byte 0

</td><td>

Magic byte.

</td></tr><tr><td>

Byte 1–4

</td><td>

Schema ID.

</td></tr><tr><td>

Remaining bytes

</td><td>

Data, serialized in an Avro format.

</td></tr></tbody>
</table>## Producers and consumers

Stream Connect producers and consumers can be configured to use an Avro format.

When configuring a producer, simply specify which schema you want to use. Then when you run the producer, the message payload is generated in JSON and automatically converted to an Avro format using the specified schema. For more information on producers, see the [Kafka Producer step](https://www.servicenow.com/docs/access?context=kafka-producer-action-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) or the [ProducerV2 API](https://www.servicenow.com/docs/access?context=ProducerV2ScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

Configuring a consumer is similar. Specify the serialization format as **Encoded** and select a schema registry. When the consumer receives a message in an Avro format, it's automatically converted to JSON according to the schema for the schema ID received in the message. For more information, see the [Kafka Message trigger](https://www.servicenow.com/docs/access?context=create-flow-kafka&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) or the [ETL](../tasks/configure-etl-consumer.md), [Transform Map](../tasks/configure-transform-map-consumer.md), or [Script](../tasks/configure-script-consumer.md) consumers.

## Plugin

Schema management features require the ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin.

-   **[Import a schema from the Confluent Registry](../tasks/import-schema-confluent-registry.md)**  
Import a Schema from the Confluent Registry to enable your Stream Connect producers and consumers to send and receive Kafka messages in an Apache Avro format.
-   **[Create a standalone schema in Stream Connect](../tasks/create-standalone-schema.md)**  
Create a schema to enable your Stream Connect producers and consumers to send and receive Kafka messages in an Apache Avro format.

**Parent Topic:**[Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md)

