---
title: Using the Stream Connect Dashboard
description: View detailed statistics for your Stream Connect integrations. Manage producers and consumers, and create or edit topics and replicators with the ServiceNow Stream Connect dashboard.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Using the Stream Connect Dashboard

View detailed statistics for your Stream Connect integrations. Manage producers and consumers, and create or edit topics and replicators with the ServiceNow® Stream Connect dashboard.

The Stream Connect Dashboard combines several capabilities into a single environment, so you can:

-   Manage multiple Stream Connect integrations through a single application.
-   Gain insights into how your integrations use and process data with detailed charts, lists, and statistics.
-   Edit topics, producers, consumers, and replicators through a simplified interface.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Workflow Data Fabric subscription

This application requires a Workflow Data Fabric subscription and a Stream Connect subscription. For more information, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

## Stream Connect Dashboard organization

To view the dashboard, navigate to **All** &gt; **Integration Hub** &gt; **Stream Connect** &gt; **Stream Connect Home**.

The dashboard has the following components.

-   Overview section
-   Topics
-   Consumers
-   Producers
-   Message Replications
-   Topic Replications

The following sections explain each component in greater detail.

## Overview section

View detailed information about your Stream Connect integrations.

![User interface for the Stream Connect dashboard overview page.](../images/stream-connect-dashboard.png "Stream Connect Dashboard Overview page")

The Overview has these components.

-   **1. Active entities section**

    Displays the number of topics, consumers, producers, and topic replicators created.

-   **2. Data usage overview**

    Displays the following charts.

    -   Consumed data: The total amount of data consumed \(in GB\).
    -   Messages processed: The total number of processed messages.
    -   Produced data: The total number of data produced \(in GB\).
    -   Messages produced: The total number of produced messages.
    -   Consumers data usage trends: The amount of data \(in MB\) consumers used over the last seven days.
    -   Producers data usage trends: The amount of data \(in MB\) producers used over the last seven days.
    You can view data for a single, selected topic, or for **All Topics** combined. You can also organize the data by time, viewing data for the **Last 24 hours**, **Last 2 days**, **Last 7 days**, or by setting a **Custom range**.


## Topics

View topics and add, edit, or export a topic.

![User interface for the Stream Connect dashboard Topics page.](../images/stream-connect-dash-topics.png "Stream Connect Dashboard Topics page")

The Topics page has the following components.

-   **3. Topics list**

    Displays all topics and each topic's name, namespace, and the date it was created.

-   **4. Action buttons**

    Contains several buttons that you can use to perform different tasks. Refresh the list of topics, edit the list columns or reset the column widths, and view or edit the list filters. There are also buttons to **Edit** a topic, **Export** a topic, and create a **New** topic.

    -   To edit a topic, select the topic from the list, select the **Edit** button, then fill in the fields on the Edit [Kafka Topic form.](https://www.servicenow.com/docs/access?context=create-topic-instance-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
    -   To create a new topic, select **New**, then fill in the fields on the Create New [Kafka Topic form.](https://www.servicenow.com/docs/access?context=create-topic-instance-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

You can select a topic from the list to view detailed information for that topic.

![User interface for an individual topic page on the Stream Connect dashboard.](../images/sc-dash-topic-page.png "Individual topic page")

Each individual topic page also has the following components.

-   **5. Topic information section**

    Displays details about the topic, including its name, namespace, status, number of partitions, date created, domain, and app ID. There’s also an **Edit** button so you can edit the topic directly from this page.

-   **6. Consumers tab in the Data Insights section**

    Displays the following charts.

    -   Messages consumed \(per minute\): The total number of messages consumed by consumers in the selected topic.
    -   Bytes consumed \(per minute\): The total number of bytes consumed.
    -   Consumer lag \(per minute\): The consumer lag in this topic group, by consumer.
    All three charts can be filtered to display data for the **Last 5 minutes**, **Last hour**, or **Last 24 hours**. When the **Last 24 hours** is selected, the data is displayed in five minutes increments instead of every minute.

    The Consumers tab also has a Consumer list, which lists the consumers associated with the topic. Each consumer is listed with its number, state, error status, max concurrency, and consumer table. You can select the consumer number to view additional details for that consumer.

-   **7. Producers tab in the Data Insights section**

    The Producers tab displays the following charts.

    -   Messages Produced: The total number of messages produced. Updated hourly.
    -   Bytes Produced in \(bytes\): The total number of bytes produced. Updated hourly.
    Both charts can be filtered to display data for the **Last 2 days**, **Last 7 days**, **Today**, **Yesterday**, or a **Custom range**.

    The Producers tab also has a Producer list, which lists the producers associated with the topic, and each producer's name, type, Id, table, and domain. You can select a producer to view additional details.

-   **8. Replications tab in the Data Insights section**

    Displays the topic replications associated with the topic, and each replication's name, topic name, direction, status, whether it's active, and error message. You can select the replication name to view additional details for that topic replication.


## Consumers

View and manage consumers.

![User interface for the Stream Connect dashboard Consumers page.](../images/stream-connect-dash-consumers.png "Stream Connect Dashboard Consumers page")

The Consumers page has the following components.

-   **9. Consumer list**

    Displays all consumers, organized by type. The possible types are:

    -   ETL
    -   Flow Trigger
    -   Script
    -   Transform Map
    Each consumer is listed with its name, number, state, associated topic, date updated, and who updated it.

-   **10. Create button**

    To **Create** a new consumer, select this button, then select the type of consumer you want to create, then fill in the fields on the consumer's form. For form field descriptions, see the [ETL consumer](../tasks/configure-etl-consumer.md), [Transform Map consumer](../tasks/configure-transform-map-consumer.md), or [Script consumer](../tasks/configure-script-consumer.md) page.

    **Note:** If you're creating a Flow Trigger consumer, there isn't a form to fill out. Instead, the dashboard opens Workflow Studio so you can build your flow trigger there. For a detailed guide, see [Create a flow with a Kafka Message trigger](https://www.servicenow.com/docs/access?context=create-flow-kafka&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).


You can select a consumer from the list to view detailed information for that consumer.

![User interface for an individual consumer page on the Stream Connect dashboard.](../images/sc-dash-consumer-page.png "Individual Consumer page")

Each individual consumer page has the following components.

-   **11. Consumer information section**

    Displays details about the consumer, including its number, status, associated topic, Kafka auto position policy, max concurrency, partition group timeout, max batch size, partitions, and an error flag.

-   **12. Overview**

    Displays the consumer's input and consumption rate, messages processed, queue depth, and any unprocessed messages. It also displays the following charts.

    -   Messages processed \(per minute\): The total number of processed messages.
    -   Message input to topic \(per minute\): The total number of messages input to the topic.
    -   Consumer lag \(per minute\): The lag for the selected consumer.
    All three charts can be filtered to display data for the **Last 5 minutes**, **Last hour**, or **Last 24 hours**. When the **Last 24 hours** is selected, the data is displayed for every five minutes instead of every minute.

-   **13. Statistics tab**

    Displays consumer statistics, including the date it was created, consumed bytes, consumed messages, produced messages, lag messages, end offset, interval, offset, and partition group.

-   **14. Logs tab**

    Displays the created logs and each log's level, message, and source.

-   **15. Partition Groups tab**

    Displays partition groups with each one's number, first and last partition, poll time, number produced per sec, queue depth, and input rate.


For a detailed explanation of consumer data and statistics, including log, and partition group information, see [Viewing Kafka subscriptions and statistics](kafka-subscriptions-statistics.md).

## Producers

View, filter, and export producers.

![User interface for the Stream Connect dashboard Producers page.](../images/stream-connect-dash-producers.png "Stream Connect Dashboard Producers page")

The Producers page has the following components.

-   **16. Producer list**

    Displays all producers and each producer's name, table, type, domain, and destination topic count.

-   **17. Action buttons**

    Contains several buttons you can use to refresh the list of producers, view or edit list filters, and **Export** a producer.


You can select a producer from the list to view detailed information for that producer.

![User interface for an individual producer page on the Stream Connect dashboard.](../images/sc-dash-producer-page.png "Individual Producer page")

Each individual consumer page has the following components.

-   **18. Producer information section**

    Displays details about the producer, including its type, ID, table, and domain. There’s also a **Manage** button. The **Manage** button redirects to the corresponding entity that produced the messages. For example, entering **Manage** on a business rule producer opens the sys\_script record. Entering **Manage** on a flow action opens that action in Workflow Studio. For background scripts, the **Manage** button is disabled because the script that was executed is not saved on the system anywhere.

-   **19. Insights**

    Displays the following data.

    -   Topics writing to: The total number of topics the producer is writing to.
    -   Messages produced rate: The average number of messages produced per second.
    -   Bytes produced rate: The average number of bytes produced per second.
    -   Undelivered messages: The total number of undelivered messages for the producer.
    -   Messages produced: Shows the number of messages produced over the last seven days.
    -   Bytes Produced: Shows the number of bytes produced over the last seven days.
    This data is updated every hour. The Messages produced and Bytes produced charts can be filtered to display data for the **Last 2 days**, **Last 24 hours**, **Last 7 days**, or a **Custom range**.

-   **20. Statistics**

    Displays producer statistics, including the date, number of produced messages and bytes, topic, and domain.


For a detailed description of Producer data and statistics, see [Viewing producer statistics](producer-statistics.md).

## Message Replications

View message replications, and add, edit, or export a message replication.

![User interface for the Stream Connect dashboard Message Replications page.](../images/stream-connect-dash-mes-rep.png "Stream Connect Dashboard Message Replications page")

The Message Replications page has the following components.

-   **21. Message Replications list**

    Displays all message replications and each replication's name, messaging service connection, status, error message \(if any\), and whether it's active.

-   **22. Action buttons**

    Contains several buttons that you can use to perform different tasks. Refresh the list of message replications, edit the list columns or reset the column widths, and view or edit the list filters. There are also buttons to **Edit** a message replication, **Export** a message replication, and create a **New** message replication.

    -   To edit a message replication, select the replication from the list, select the **Edit** button, then fill in the fields on the Edit [Message Replication form](../tasks/configure-message-topic-reps-sc.md).
    -   To create a new message replication, select **New**, then fill in the fields on the Create New [Message Replication form](../tasks/configure-message-topic-reps-sc.md).

You can select a message replication to view the replication's name, messaging service connection, status, error message \(if any\), and if it's active. You can also see any associated Kafka Topic Replications.

## Topic Replications

View topic replications, and add, edit, or export a topic replication.

![User interface for the Stream Connect dashboard Topic Replications page.](../images/stream-connect-dash-topic-rep.png "Stream Connect Dashboard Topic Replications page")

The Topic Replications page has the following components.

-   **23. Topic Replications list**

    Displays all topic replications, and each replication's name, direction, replication, topic name, ServiceNow topic, status, error message \(if any\), whether it's active, and whether it's being tracked in the current update set.

-   **24. Action buttons**

    Contains several buttons you can use to refresh the list of topic replications, edit the list columns or reset the column widths, and view or edit the list filters. There are also buttons to **Edit** a topic replication, **Export** a topic replication, and create a **New** topic replication.

    -   To edit a topic replication, select the replication from the list, select the **Edit** button, then fill in the fields on the Edit [Topic Replication form](../tasks/configure-message-topic-reps-sc.md).
    -   To create a new topic replication, select **New**, then fill in the fields on the Create New [Topic Replication form](../tasks/configure-message-topic-reps-sc.md).

You can select a topic replication to view its name, direction, replication, topic name, ServiceNow topic, status, error message \(if any\), if it's active, and if it's being tracked in the current update set. You can also see any associated [Message Replication statistics](../reference/stream-connect-message-rep-stats.md).

**Parent Topic:**[Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md)

