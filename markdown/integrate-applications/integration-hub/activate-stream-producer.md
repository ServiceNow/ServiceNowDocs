---
title: Activate or deactivate a Stream Producer
description: Activate a Stream Producer configuration to begin capturing and streaming table changes to your Kafka topic. You can deactivate it at any time to stop streaming changes. When you deactivate a producer, any unprocessed messages in the CDC queue are discarded.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/activate-stream-producer.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 2
keywords: [activate, deactivate, Stream Producer, start, stop]
breadcrumb: [Stream Producer, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Activate or deactivate a Stream Producer

Activate a Stream Producer configuration to begin capturing and streaming table changes to your Kafka topic. You can deactivate it at any time to stop streaming changes. When you deactivate a producer, any unprocessed messages in the CDC queue are discarded.

## Before you begin

Before you begin:

-   A Stream Producer configuration must exist.
-   All required form fields must be completed.

Role required: `kafka_producer`

## About this task

When you activate a Stream Producer, the change data capture \(CDC\) listener starts monitoring the specified table for changes. Any matching table changes are immediately captured and sent to the target Kafka topic. When you deactivate the producer, monitoring stops and no new messages are sent.

**Important:** When you deactivate a Stream Producer, any unprocessed messages that are currently staged in the CDC queue won't be sent to Kafka. This is the expected behavior to prevent sending stale or outdated events when the producer is reactivated later. When it's reactivated, only new changes \(from the moment of reactivation onward\) will be captured and sent.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Stream Producers**.

2.  In the Stream Producer list, locate and select the producer you want to activate or deactivate.

3.  To activate the producer:

    1.  In the Related Links section, select **Activate** \(available only if the producer is currently inactive\).

        The Stream Producer starts monitoring the table. The **Active** field is automatically set to `true`. A corresponding Kafka Producer record is created and appears in the **Kafka Producer** related list.

4.  To deactivate the producer:

    1.  In the Related Links section, select **Deactivate** \(available only if the producer is currently active\).

        A confirmation dialog appears warning you that deactivating the producer will stop all events from being published to the Kafka topic and listing the number of events currently staged in the CDC queue that will be discarded.

    2.  Select **OK** to confirm deactivation, or **Cancel** to cancel.

        If you select **OK**: The Stream Producer stops monitoring the table. The **Active** field is automatically set to `false`. All staged messages in the CDC queue are discarded and will not be sent to the Kafka topic. No new messages are sent to Kafka.


## Result

The Stream Producer is activated or deactivated as requested. If you activated the producer, it begins streaming table changes immediately. If you deactivated it, streaming stops.

## What to do next

After activating a Stream Producer, you can monitor activity and metrics in the **Stream Producer CDC Statistics** related list on the Stream Producer form. Statistics are updated periodically and show the number of messages sent and other activity metrics.

**Parent Topic:**[Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/stream-producer.md)

