---
title: Exchanging data using Hermes
description: Produce and consume Kafka messages in your ServiceNow instance using the Hermes Messaging Service.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Exchanging data using Hermes

Produce and consume Kafka messages in your ServiceNow instance using the Hermes Messaging Service.

There are several methods for exchanging data between your ServiceNow instance and your Kafka environment using the Hermes Messaging Service. In all cases, data is produced from one entity and consumed by another.

## Using Stream Connect

With Stream Connect, you can produce messages from your ServiceNow instance using a Producer step from a flow action or the Producer API, and then consume the messages in your external application.

You can also produce messages from an external application and then consume the messages in your ServiceNow instance via any of the following methods:

-   Kafka flow trigger
-   ETL consumer
-   Transform map consumer
-   Script consumer

![Producing and consuming with Stream Connect for Apache Kafka.](../../integrationhub/images/stream-connect.png "Stream Connect overview")

For details, see [Stream Connect for Apache Kafka](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

## Using Log Export Service

With the Log Export Service, you can produce logs from your ServiceNow instance, and then consume the logs in your external application.

![Log Export Service architecture.](../../log-export-service/image/les-architecture.png "Log Export Service architecture")

For details on producing and consuming logs for Log Export Service, see [Exploring Log Export Service \(LES\)](https://www.servicenow.com/docs/access?context=les-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Using a Kafka client

With the Kafka standard protocol, you can exchange messages with any application that produces messages. For example, you can produce messages from a Java application using the standard Kafka protocol and then consume them in your ServiceNow instance and vice versa.

![Producing and consuming messages with Advanced High Availability (AHA).](../images/hermes-producing-consuming.png "Producing and consuming messages")

For details on exchanging data using a Kafka client, see [Producing and consuming messages from a Kafka client](producing-consuming-hermes.md).

**Parent Topic:**[Manage service capabilities](../../general/concept/manage-services.md)

