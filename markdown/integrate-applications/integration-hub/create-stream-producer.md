---
title: Create a Stream Producer
description: Create a Stream Producer configuration to automatically stream table changes to a Kafka topic. You can specify which table to monitor, which change events to capture, which fields to include, and configure keys and headers for routing and tracking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/create-stream-producer.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 5
keywords: [create, Stream Producer, producer configuration, Kafka topic]
breadcrumb: [Stream Producer, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Create a Stream Producer

Create a Stream Producer configuration to automatically stream table changes to a Kafka topic. You can specify which table to monitor, which change events to capture, which fields to include, and configure keys and headers for routing and tracking.

## Before you begin

Before you begin:

-   Verify that you have access to the Stream Connect application.
-   Identify the table you want to monitor.
-   Verify that a Kafka topic exists to receive the stream data.

Role required: `kafka_producer`

## About this task

Create a Stream Producer configuration to define how ServiceNow captures and streams changes from a specific table. After you create and activate the configuration, the Stream Producer automatically sends matching table changes to your Kafka topic with optional keys and headers for enhanced message routing.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Stream Producers**.

2.  Select **New**.

3.  On the Stream Producer form, fill in the fields.

<table id="table_bgl_mdz_vjc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this producer configuration. The name identifies the producer in the Stream Producer list and must be unique within the Stream Producer \[`sys_sc_stream_producer`\] table.

</td></tr><tr><td>

Application

</td><td>

Application scope for the producer. This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the Stream Producer is currently active.

 When a Stream Producer is first configured, it is inactive by default. You can activate the producer after it's configured.

</td></tr><tr><td>

Table Name

</td><td>

Name of the ServiceNow table you want to monitor for changes. Stream Producer captures inserts, updates, and deletes on this table.

</td></tr><tr><td>

Filter

</td><td>

Option to apply filters to restrict which records trigger the producer.

 Select **Add filter Condition** to create filters. You can add multiple conditions using AND/OR logic.

 Filter examples:

-   `Location = London`
-   `State = Active AND Location = London`


</td></tr><tr><td>

Capture all fields

</td><td>

Option to include every field from the table in the message payload. Selected by default. You can unselect to choose specific fields.

</td></tr><tr><td>

Fields

</td><td>

Fields to include in the payload. Use the slush bucket to add or remove fields. At least one field must be selected.

 The Sys ID is mandatory and is included in the record, even if the field selection is empty.

 This field only appears if **Capture all Fields** is not selected \(is not checked\).

 **Note:** Sensitive field types \(password, password2, glide\_encrypted\) are automatically excluded from all message payloads and schemas, regardless of whether they are selected. These fields aren't sent to Kafka to protect sensitive information.

</td></tr><tr><td>

On Insert

</td><td>

Option to configure which change events trigger the producer. When checked, **On Insert** captures new record insertions in the selected table.

</td></tr><tr><td>

On Update

</td><td>

Option to configure which change events trigger the producer. When checked, **On Update** captures updates to existing records in the selected table.

</td></tr><tr><td>

On Delete

</td><td>

Option to configure which change events trigger the producer. When checked, **On Delete** captures record deletions in the selected table.

</td></tr><tr><td>

Only trigger update if any selected field has changed

</td><td>

If enabled, update events only trigger when at least one of the selected fields has changed.

 This field can only be selected if **On Update** is also selected.

</td></tr><tr><td>

Topic Alias

</td><td>

The alias for the target Kafka topic. This is the topic that receives the stream data. Select from existing topics in your Kafka environment.

</td></tr><tr><td>

Key Selection

</td><td>

Select a key for the payload.

 The key is a single field value \(or combination with a prefix\) that determines which partition a message goes to in Kafka.

 Topics can be partitioned. Messages with the same key go to the same partition. This assists with the ordering of related messages.

 Common choices: Sys ID, incident number, request number, or any unique identifier in your table. Reference fields are supported; the ID value \(not the display name\) is used as the key.

</td></tr><tr><td>

Key Prefix

</td><td>

Option to select the type of key prefix. Choose one of the following.-   **No prefix**: The default value. No prefix is added to the key. Example: `0a666274c3f1ba10d14320bdc00131dc`
-   **Instance Name**: The key is prefixed with the name of the instance. Example: `streamconnectdemo:0a666274c3f1ba10d14320bdc00131dc`
-   **Custom**: The key is prefixed to the value of your choosing. Example: `abc123-0a666274c3f1ba10d14320bdc00131dc`


</td></tr><tr><td>

Prefix

</td><td>

Prefix for the Key.

 This field only appears if **Key Prefix** is set to **Instance Name** or **Custom**.

-   If you selected **Instance Name**, it's automatically set to the name of the instance.
-   If you selected **Custom**, enter the prefix of your choice, up to 100 characters.


</td></tr><tr><td>

Header Selection

</td><td>

Select one or more fields to include as Kafka message headers. Headers are key-value pairs that carry metadata about the change event and are useful for routing and filtering in downstream systems.

 By default, Stream Producer automatically adds the following system headers to every message.

 -   `action`: The type of change \(insert, update, or delete\).
-   `collection_timestamp_ms`: The timestamp when the change was captured.
-   `table_name`: The name of the source table.
 You can select any number of fields from your source table. For each custom header field you select:

 -   Simple fields \(text, numbers, dates\) are sent as-is. Example: `number: INC0000001`
-   Reference fields \(links to other tables\) include both the ID and display name. Example: `assigned_to: c39e3639876aba141444337e0ebb354f:Bob Person`
-   Choice fields \(dropdown values\) include both the value and display name. Example header: `"state": "1:New"`


</td></tr><tr><td>

Serialization Format

</td><td>

Option to specify how the message payload is formatted. Select **JSON** for plain text messages or **Encoded - Avro** to send messages in Apache Avro binary format with an embedded schema.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The Stream Producer configuration is created and ready to activate. The configuration appears in the Stream Producer list.

In the Related Links section of the form, there is a **Show Payload** option where you can select a record to view a sample JSON payload with a key, headers, and size.

If the **Serialization Format** is **Encoded - Avro** the Related Links section has a **View Schema** option where you can see the Table Message Schema Evolution form associated with the producer.

## What to do next

To begin capturing and streaming table changes, activate the Stream Producer. See [Activate or deactivate a Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/activate-stream-producer.md) for instructions.

**Parent Topic:**[Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/stream-producer.md)

